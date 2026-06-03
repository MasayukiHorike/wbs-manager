<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>WBS Manager</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@400;500&family=Syne:wght@600;700;800&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#F7F6F3;
  --surface:#FFFFFF;
  --surface2:#F0EEE9;
  --border:#E2DFDA;
  --border2:#CCC9C2;
  --text:#1A1917;
  --text2:#6B6860;
  --text3:#9B9890;
  --accent:#2563EB;
  --accent-light:#EEF3FF;
  --accent2:#7C3AED;
  --success:#059669;
  --success-light:#ECFDF5;
  --warn:#D97706;
  --warn-light:#FFFBEB;
  --danger:#DC2626;
  --danger-light:#FEF2F2;
  --shadow:0 1px 3px rgba(0,0,0,.08),0 1px 2px rgba(0,0,0,.05);
  --shadow-md:0 4px 12px rgba(0,0,0,.08),0 2px 4px rgba(0,0,0,.05);
  --radius:8px;
  --radius-sm:5px;
}
body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text);font-size:14px;line-height:1.5;min-height:100vh;overflow-x:hidden}

/* ─── Header ─── */
.app-header{background:var(--surface);border-bottom:1px solid var(--border);padding:0 24px;height:56px;display:flex;align-items:center;gap:16px;position:sticky;top:0;z-index:100}
.app-logo{font-family:'Syne',sans-serif;font-weight:800;font-size:18px;letter-spacing:-.5px;color:var(--text)}
.app-logo span{color:var(--accent)}
.header-divider{width:1px;height:24px;background:var(--border);margin:0 4px}
.header-tabs{display:flex;gap:4px}
.tab-btn{padding:6px 14px;border-radius:var(--radius-sm);border:none;background:none;color:var(--text2);font-family:'DM Sans',sans-serif;font-size:13px;font-weight:500;cursor:pointer;transition:.15s}
.tab-btn:hover{background:var(--surface2);color:var(--text)}
.tab-btn.active{background:var(--accent);color:#fff}
.header-spacer{flex:1}
.header-actions{display:flex;gap:8px;align-items:center}
.btn{display:inline-flex;align-items:center;gap:6px;padding:7px 14px;border-radius:var(--radius-sm);border:1px solid var(--border);background:var(--surface);color:var(--text);font-family:'DM Sans',sans-serif;font-size:13px;font-weight:500;cursor:pointer;transition:.15s;white-space:nowrap}
.btn:hover{background:var(--surface2);border-color:var(--border2)}
.btn-primary{background:var(--accent);color:#fff;border-color:var(--accent)}
.btn-primary:hover{background:#1d4ed8;border-color:#1d4ed8}
.btn-sm{padding:5px 10px;font-size:12px}

/* ─── Layout ─── */
.app-body{display:flex;height:calc(100vh - 56px)}
.sidebar{width:260px;flex-shrink:0;background:var(--surface);border-right:1px solid var(--border);overflow-y:auto;overflow-x:hidden;padding:16px;transition:width .25s cubic-bezier(.4,0,.2,1),padding .25s;position:relative}
.sidebar.collapsed{width:48px;padding:12px 0;overflow-y:hidden}
.sidebar.collapsed .sidebar-content{opacity:0;pointer-events:none;transition:opacity .1s}
.sidebar-content{transition:opacity .2s .05s}
.sidebar-toggle{position:absolute;top:12px;right:10px;width:26px;height:26px;border:1px solid var(--border);border-radius:var(--radius-sm);background:var(--surface);cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:12px;color:var(--text3);transition:.15s;z-index:10;flex-shrink:0}
.sidebar-toggle:hover{background:var(--surface2);color:var(--text);border-color:var(--border2)}
.sidebar.collapsed .sidebar-toggle{right:50%;transform:translateX(50%);top:12px}
.sidebar-collapsed-icons{display:none;flex-direction:column;align-items:center;gap:14px;padding-top:48px}
.sidebar.collapsed .sidebar-collapsed-icons{display:flex}
.collapsed-stat{display:flex;flex-direction:column;align-items:center;gap:2px}
.collapsed-stat-num{font-family:'Syne',sans-serif;font-size:16px;font-weight:700;color:var(--text);line-height:1}
.collapsed-stat-dot{width:6px;height:6px;border-radius:50%;margin-top:2px}
.main-area{flex:1;overflow:hidden;display:flex;flex-direction:column}
.toolbar{padding:12px 20px;background:var(--surface);border-bottom:1px solid var(--border);display:flex;align-items:center;gap:10px;flex-wrap:wrap}
.search-box{display:flex;align-items:center;gap:8px;background:var(--surface2);border:1px solid var(--border);border-radius:var(--radius-sm);padding:6px 10px;flex:1;max-width:280px}
.search-box input{border:none;background:none;outline:none;font-family:'DM Sans',sans-serif;font-size:13px;color:var(--text);width:100%}
.filter-select{padding:6px 10px;border:1px solid var(--border);border-radius:var(--radius-sm);background:var(--surface);font-family:'DM Sans',sans-serif;font-size:13px;color:var(--text);outline:none;cursor:pointer}

/* ─── WBS Table ─── */
.wbs-container{flex:1;overflow:auto;padding:20px}
.wbs-table{width:100%;border-collapse:separate;border-spacing:0;min-width:900px}
.wbs-table th{background:var(--surface2);padding:9px 12px;text-align:left;font-size:11px;font-weight:600;text-transform:uppercase;letter-spacing:.06em;color:var(--text3);border-bottom:2px solid var(--border);white-space:nowrap;position:sticky;top:0;z-index:10}
.wbs-table th:first-child{border-radius:var(--radius) 0 0 0}
.wbs-table th:last-child{border-radius:0 var(--radius) 0 0}
.wbs-table td{padding:0;border-bottom:1px solid var(--border);vertical-align:middle}
.task-row{transition:background .1s}
.task-row:hover{background:#FAFAF8}
.task-row.selected{background:var(--accent-light)}
.task-row.level-0>.td-name>.task-name-inner{font-weight:600;font-size:13px}
.task-row.level-1>.td-name>.task-name-inner{font-size:13px}
.task-row.level-2>.td-name>.task-name-inner{font-size:12.5px;color:var(--text2)}

.td-name{padding:8px 12px;display:flex;align-items:center;gap:6px;min-width:280px;max-width:380px}
.indent-spacer{display:inline-block;width:20px;flex-shrink:0}
.toggle-btn{width:18px;height:18px;border:none;background:none;cursor:pointer;display:flex;align-items:center;justify-content:center;border-radius:3px;flex-shrink:0;color:var(--text3);transition:.1s}
.toggle-btn:hover{background:var(--surface2);color:var(--text)}
.toggle-btn.leaf{cursor:default;opacity:0}
.task-icon{font-size:13px;flex-shrink:0}
.task-name-inner{display:flex;flex-direction:column;gap:1px;min-width:0}
.task-name-text{white-space:nowrap;overflow:hidden;text-overflow:ellipsis;cursor:pointer}
.task-name-text:hover{color:var(--accent)}
.task-deliverable{font-size:11px;color:var(--text3);font-style:italic;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}

td.td-cell{padding:8px 12px;white-space:nowrap}
.status-badge{display:inline-flex;align-items:center;gap:5px;padding:3px 8px;border-radius:20px;font-size:11px;font-weight:500}
.s-todo{background:#F1F0EC;color:var(--text2)}
.s-doing{background:var(--warn-light);color:var(--warn)}
.s-done{background:var(--success-light);color:var(--success)}
.s-block{background:var(--danger-light);color:var(--danger)}

.progress-wrap{display:flex;align-items:center;gap:8px;min-width:120px}
.progress-bar{flex:1;height:5px;background:var(--surface2);border-radius:3px;overflow:hidden}
.progress-fill{height:100%;border-radius:3px;transition:.3s}
.progress-text{font-size:11px;color:var(--text3);font-family:'DM Mono',monospace;width:28px;text-align:right}

.assignee-chip{display:inline-flex;align-items:center;gap:5px;font-size:12px}
.avatar{width:22px;height:22px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:10px;font-weight:600;color:#fff;flex-shrink:0}
.date-text{font-size:12px;font-family:'DM Mono',monospace;color:var(--text2)}
.date-text.overdue{color:var(--danger)}
.date-text.today{color:var(--warn);font-weight:600}
.dep-list{display:flex;gap:4px;flex-wrap:wrap}
.dep-chip{padding:2px 6px;background:var(--surface2);border:1px solid var(--border);border-radius:4px;font-size:10px;font-family:'DM Mono',monospace;color:var(--text2)}

.row-actions{display:flex;gap:4px;opacity:0;transition:.1s}
.task-row:hover .row-actions{opacity:1}
.icon-btn{width:26px;height:26px;border:none;background:none;border-radius:4px;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:13px;color:var(--text3);transition:.1s}
.icon-btn:hover{background:var(--surface2);color:var(--text)}

/* ─── Sidebar ─── */
.sidebar-section{margin-bottom:24px}
.sidebar-label{font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.08em;color:var(--text3);margin-bottom:10px}
.stat-card{background:var(--surface2);border-radius:var(--radius);padding:12px;margin-bottom:8px}
.stat-num{font-family:'Syne',sans-serif;font-size:24px;font-weight:700;color:var(--text);line-height:1}
.stat-label{font-size:11px;color:var(--text3);margin-top:3px}
.mini-progress{height:4px;background:var(--border);border-radius:2px;margin-top:8px;overflow:hidden}
.mini-fill{height:100%;border-radius:2px;background:var(--accent);transition:.5s}

.legend-item{display:flex;align-items:center;gap:8px;padding:5px 0;font-size:12px;color:var(--text2)}
.legend-dot{width:8px;height:8px;border-radius:50%;flex-shrink:0}

/* ─── Gantt ─── */
.gantt-wrapper{flex:1;overflow:hidden;padding:20px;display:flex;flex-direction:column;min-height:0}
.gantt-wrapper #gantt-inner{flex:1;display:flex;flex-direction:column;min-height:0;overflow:hidden}
.gantt-container{display:flex;min-width:100%}
.gantt-tasks{flex-shrink:0;width:260px;background:var(--surface);border-right:1px solid var(--border);border-radius:var(--radius) 0 0 var(--radius)}
.gantt-chart{flex:1;overflow:auto;min-width:0}
.gantt-header-row{display:flex;background:var(--surface2);border-bottom:2px solid var(--border);position:sticky;top:0;z-index:5}
.gantt-task-header{width:260px;flex-shrink:0;padding:9px 16px;font-size:11px;font-weight:600;text-transform:uppercase;letter-spacing:.06em;color:var(--text3);border-bottom:2px solid var(--border);background:var(--surface2)}
.gantt-col-header{padding:9px 0;font-size:11px;font-weight:500;color:var(--text3);text-align:center;border-left:1px solid var(--border);white-space:nowrap}
.gantt-task-row{display:flex;align-items:stretch;border-bottom:1px solid var(--border)}
.gantt-task-label{width:260px;flex-shrink:0;padding:10px 16px;font-size:12px;font-weight:500;display:flex;align-items:center;gap:6px;border-right:1px solid var(--border);background:var(--surface)}
.gantt-row-cells{flex:1;display:flex;position:relative;min-height:38px}
.gantt-cell{border-left:1px solid var(--border);flex:0 0 var(--day-w);position:relative}
.gantt-cell.weekend{background:#FAFAF8}
.gantt-cell.today-col{background:#EEF3FF}
.gantt-bar-wrap{position:absolute;top:7px;height:24px;display:flex;align-items:center;z-index:2;pointer-events:none}
.gantt-bar{height:20px;border-radius:4px;display:flex;align-items:center;padding:0 8px;font-size:10px;font-weight:500;color:#fff;white-space:nowrap;overflow:hidden;min-width:4px}
.today-line{position:absolute;top:0;bottom:0;width:2px;background:var(--accent);z-index:10;pointer-events:none}

/* ─── Detail Panel ─── */
.detail-panel{position:fixed;right:0;top:56px;width:360px;height:calc(100vh - 56px);background:var(--surface);border-left:1px solid var(--border);box-shadow:var(--shadow-md);transform:translateX(100%);transition:.25s cubic-bezier(.4,0,.2,1);overflow-y:auto;z-index:200}
.detail-panel.open{transform:translateX(0)}
.detail-header{padding:20px 20px 16px;border-bottom:1px solid var(--border);display:flex;align-items:flex-start;gap:12px}
.detail-title-wrap{flex:1}
.detail-title{font-family:'Syne',sans-serif;font-size:17px;font-weight:700;line-height:1.3}
.detail-wbs-id{font-size:11px;font-family:'DM Mono',monospace;color:var(--text3);margin-top:3px}
.detail-close{border:none;background:none;cursor:pointer;font-size:18px;color:var(--text3);padding:2px;line-height:1;transition:.1s}
.detail-close:hover{color:var(--text)}
.detail-body{padding:20px}
.detail-section{margin-bottom:20px}
.detail-section-label{font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.08em;color:var(--text3);margin-bottom:10px}
.detail-field{margin-bottom:12px}
.detail-field label{display:block;font-size:11px;color:var(--text3);margin-bottom:5px;font-weight:500}
.detail-field input,.detail-field select,.detail-field textarea{width:100%;padding:8px 10px;border:1px solid var(--border);border-radius:var(--radius-sm);font-family:'DM Sans',sans-serif;font-size:13px;color:var(--text);background:var(--surface);outline:none;transition:.15s}
.detail-field input:focus,.detail-field select:focus,.detail-field textarea:focus{border-color:var(--accent);box-shadow:0 0 0 3px rgba(37,99,235,.1)}
.detail-field textarea{resize:vertical;min-height:70px}
.detail-actions{display:flex;gap:8px;padding:16px 20px;border-top:1px solid var(--border)}

/* ─── Modal ─── */
.modal-overlay{position:fixed;inset:0;background:rgba(0,0,0,.3);z-index:500;display:none;align-items:center;justify-content:center}
.modal-overlay.open{display:flex}
.modal-overlay.z-top{z-index:1100}  /* ログイン画面より前面 */
.modal{background:var(--surface);border-radius:var(--radius);box-shadow:var(--shadow-md);width:520px;max-width:95vw;max-height:90vh;overflow-y:auto;padding:28px}
.modal-title{font-family:'Syne',sans-serif;font-size:20px;font-weight:700;margin-bottom:20px}
.modal-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px}
.modal-grid .full{grid-column:1/-1}
.form-field{display:flex;flex-direction:column;gap:5px}
.form-field label{font-size:11px;font-weight:600;text-transform:uppercase;letter-spacing:.06em;color:var(--text3)}
.form-field input,.form-field select,.form-field textarea{padding:8px 10px;border:1px solid var(--border);border-radius:var(--radius-sm);font-family:'DM Sans',sans-serif;font-size:13px;color:var(--text);background:var(--surface);outline:none;transition:.15s}
.form-field input:focus,.form-field select:focus,.form-field textarea:focus{border-color:var(--accent);box-shadow:0 0 0 3px rgba(37,99,235,.1)}
.form-field textarea{resize:vertical;min-height:60px}
.modal-footer{display:flex;justify-content:flex-end;gap:10px;margin-top:24px}

/* ─── Empty ─── */
.empty-state{display:flex;flex-direction:column;align-items:center;justify-content:center;padding:60px 20px;color:var(--text3);gap:12px}
.empty-state .icon{font-size:40px;opacity:.4}
.empty-state p{font-size:14px}

/* ─── Range slider ─── */
input[type=range]{-webkit-appearance:none;width:100%;height:4px;border-radius:2px;background:var(--border);outline:none}
input[type=range]::-webkit-slider-thumb{-webkit-appearance:none;width:14px;height:14px;border-radius:50%;background:var(--accent);cursor:pointer}

/* ─── Context Menu ─── */
.ctx-item{display:flex;align-items:center;gap:10px;width:100%;padding:9px 14px;border:none;background:none;font-family:'DM Sans',sans-serif;font-size:13px;color:var(--text);cursor:pointer;text-align:left;transition:.1s;position:relative}
.ctx-item:hover{background:var(--surface2)}
.ctx-hint{margin-left:auto;font-size:10px;background:var(--surface2);border:1px solid var(--border);border-radius:3px;padding:1px 5px;color:var(--text3);font-family:'DM Mono',monospace}
.add-sibling-btn,.add-child-btn{border-radius:4px!important;height:24px!important;font-family:'DM Sans',monospace;letter-spacing:-.2px;transition:.15s!important}
.add-sibling-btn:hover{background:var(--surface2)!important;color:var(--text)!important}
.add-child-btn:hover{background:var(--accent-light)!important;color:var(--accent)!important}
.row-actions .icon-btn:last-child:hover{background:var(--danger-light)!important;color:var(--danger)!important}

/* ─── Project selector ─── */
.proj-selector{display:flex;align-items:center;gap:8px;background:var(--surface2);border:1px solid var(--border);border-radius:var(--radius-sm);padding:4px 6px 4px 10px;max-width:240px;min-width:140px}
.proj-selector select{border:none;background:none;outline:none;font-family:'DM Sans',sans-serif;font-size:13px;font-weight:500;color:var(--text);cursor:pointer;flex:1;min-width:0}
.proj-color-dot{width:8px;height:8px;border-radius:50%;flex-shrink:0}

/* ─── Project list in sidebar ─── */
.proj-list-item{display:flex;align-items:center;gap:8px;padding:7px 10px;border-radius:var(--radius-sm);cursor:pointer;transition:.12s;border:1px solid transparent}
.proj-list-item:hover{background:var(--surface2)}
.proj-list-item.active{background:var(--accent-light);border-color:#BFDBFE}
.proj-list-item .proj-dot{width:10px;height:10px;border-radius:50%;flex-shrink:0}
.proj-list-item .proj-name{font-size:13px;font-weight:500;flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.proj-list-item .proj-count{font-size:10px;color:var(--text3);font-family:'DM Mono',monospace;flex-shrink:0}
.proj-list-item .proj-actions{display:none;gap:2px;flex-shrink:0}
.proj-list-item:hover .proj-actions{display:flex}
.proj-edit-input{border:1px solid var(--accent);border-radius:3px;padding:2px 6px;font-size:13px;font-family:'DM Sans',sans-serif;outline:none;flex:1;min-width:0}

/* ─── User switcher ─── */
.user-btn{display:flex;align-items:center;gap:8px;padding:4px 10px 4px 4px;border:1px solid var(--border);border-radius:20px;background:var(--surface);cursor:pointer;transition:.15s;font-family:'DM Sans',sans-serif;font-size:13px;font-weight:500;color:var(--text)}
.user-btn:hover{background:var(--surface2);border-color:var(--border2)}
.user-btn .avatar-lg{width:28px;height:28px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:700;color:#fff;flex-shrink:0}

/* ─── User switcher dropdown ─── */
.user-panel{position:fixed;top:62px;right:16px;width:300px;background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);box-shadow:var(--shadow-md);z-index:300;overflow:hidden;display:none}
.user-panel.open{display:block}
.user-panel-header{padding:14px 16px 10px;border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between}
.user-panel-title{font-size:12px;font-weight:600;text-transform:uppercase;letter-spacing:.06em;color:var(--text3)}
.user-list{max-height:280px;overflow-y:auto}
.user-item{display:flex;align-items:center;gap:10px;padding:10px 14px;cursor:pointer;transition:.12s;border-bottom:1px solid var(--border)}
.user-item:last-child{border-bottom:none}
.user-item:hover{background:var(--surface2)}
.user-item.active{background:var(--accent-light)}
.user-item .uavatar{width:34px;height:34px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:700;color:#fff;flex-shrink:0;position:relative}
.user-item .uavatar .online-dot{position:absolute;bottom:0;right:0;width:9px;height:9px;border-radius:50%;background:var(--success);border:2px solid var(--surface)}
.user-item-info{flex:1;min-width:0}
.user-item-name{font-size:13px;font-weight:500;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.user-item-meta{font-size:11px;color:var(--text3);margin-top:1px}
.user-item-actions{display:none;gap:2px}
.user-item:hover .user-item-actions{display:flex}
.user-panel-footer{padding:10px 14px;border-top:1px solid var(--border);display:flex;gap:8px}

/* ─── User management modal ─── */
.user-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.user-grid .full{grid-column:1/-1}
.color-swatch{width:26px;height:26px;border-radius:50%;cursor:pointer;border:3px solid transparent;transition:.12s;flex-shrink:0}
.color-swatch.selected{border-color:#1A1917}

/* ─── Login screen ─── */
.login-screen{position:fixed;inset:0;background:var(--bg);z-index:999;display:flex;align-items:center;justify-content:center}
.login-card{background:var(--surface);border:1px solid var(--border);border-radius:12px;box-shadow:var(--shadow-md);padding:40px;width:400px;max-width:95vw}
.login-logo{font-family:'Syne',sans-serif;font-weight:800;font-size:28px;color:var(--text);margin-bottom:6px}
.login-logo span{color:var(--accent)}
.login-sub{font-size:13px;color:var(--text3);margin-bottom:28px}
.login-user-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:24px}
.login-user-card{padding:14px 12px;border:1px solid var(--border);border-radius:var(--radius);cursor:pointer;transition:.15s;display:flex;flex-direction:column;align-items:center;gap:8px;background:var(--surface)}
.login-user-card:hover{border-color:var(--accent);background:var(--accent-light);transform:translateY(-1px);box-shadow:var(--shadow)}
.login-user-card .l-avatar{width:44px;height:44px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:16px;font-weight:700;color:#fff}
.login-user-card .l-name{font-size:13px;font-weight:500;text-align:center}
.login-user-card .l-role{font-size:11px;color:var(--text3)}

/* ─── Sort mode ─── */
.sort-mode-active .task-row{cursor:default}
.drag-handle{width:18px;height:24px;display:none;align-items:center;justify-content:center;cursor:grab;color:var(--text3);font-size:14px;flex-shrink:0;border-radius:3px;transition:.1s;user-select:none}
.drag-handle:hover{background:var(--surface2);color:var(--text)}
.drag-handle:active{cursor:grabbing}
.sort-mode-active .drag-handle{display:flex}
/* 並替モードON時はボタンを隠す */
.sort-mode-active .row-actions{display:none!important}
.sort-mode-active .task-row.dragging{opacity:.4;background:var(--surface2)!important}
.sort-mode-active .task-row.drag-over-above td:first-child{box-shadow:inset 0 2px 0 var(--accent)}
.sort-mode-active .task-row.drag-over-below td:first-child{box-shadow:inset 0 -2px 0 var(--accent)}
.drop-indicator{height:3px;background:var(--accent);border-radius:2px;margin:0;display:none;position:relative}
.drop-indicator::before{content:'';position:absolute;left:0;top:-4px;width:10px;height:10px;border-radius:50%;background:var(--accent)}
.drop-indicator.visible{display:block}
.sort-toggle-btn.active{background:var(--warn-light)!important;border-color:var(--warn)!important;color:var(--warn)!important}

/* ─── 参照モード / 編集モード ─── */
.readonly-banner{display:none;align-items:center;gap:8px;padding:4px 12px;background:#FFFBEB;border:1px solid #FCD34D;border-radius:var(--radius-sm);font-size:12px;font-weight:500;color:#92400E;white-space:nowrap}
.readonly-banner.visible{display:flex}
.checkin-btn{background:#059669!important;border-color:#059669!important;color:#fff!important}
.checkin-btn:hover{background:#047857!important;border-color:#047857!important}
.checkout-btn{background:var(--warn)!important;border-color:var(--warn)!important;color:#fff!important}
.checkout-btn:hover{background:#B45309!important;border-color:#B45309!important}
/* 参照モード時：編集系UI を無効化 */
body.readonly-mode .btn-primary{opacity:.4;pointer-events:none}
body.readonly-mode .row-actions{opacity:.2;pointer-events:none}
body.readonly-mode .drag-handle{opacity:.2;pointer-events:none}
body.readonly-mode .gantt-bar[data-action]{cursor:default!important;pointer-events:none}
body.readonly-mode .gantt-resize-handle{pointer-events:none}
body.readonly-mode .add-child-btn,body.readonly-mode .add-sibling-btn{opacity:.2;pointer-events:none}
body.readonly-mode #sort-toggle-btn{opacity:.4;pointer-events:none}
body.readonly-mode .detail-actions button:not(.btn-primary+button):first-child{opacity:.4;pointer-events:none}

/* ─── Storage mode indicator ─── */
.storage-indicator{display:flex;align-items:center;gap:6px;padding:4px 10px;border-radius:var(--radius-sm);font-size:12px;font-weight:500;border:1px solid var(--border);background:var(--surface2);cursor:pointer;transition:.15s;white-space:nowrap}
.storage-indicator:hover{background:var(--surface);border-color:var(--border2)}
.storage-indicator.mode-csv{background:#ECFDF5;border-color:#6EE7B7;color:#065F46}
.storage-indicator.mode-ls{background:var(--surface2);color:var(--text2)}
.storage-indicator.mode-error{background:#FEF2F2;border-color:#FCA5A5;color:var(--danger)}
.storage-dot{width:7px;height:7px;border-radius:50%;flex-shrink:0}

/* ─── Storage settings modal ─── */
.storage-option{display:flex;align-items:flex-start;gap:12px;padding:14px;border:2px solid var(--border);border-radius:var(--radius);cursor:pointer;transition:.15s;margin-bottom:10px}
.storage-option:hover{border-color:var(--border2);background:var(--surface2)}
.storage-option.selected{border-color:var(--accent);background:var(--accent-light)}
.storage-option-icon{font-size:24px;flex-shrink:0;line-height:1}
.storage-option-title{font-size:13px;font-weight:600;margin-bottom:3px}
.storage-option-desc{font-size:11px;color:var(--text3);line-height:1.5}

/* ─── Help modal ─── */
.help-modal{width:760px;max-width:96vw;max-height:86vh;display:flex;flex-direction:column;padding:0;overflow:hidden}
.help-tabs{display:flex;border-bottom:2px solid var(--border);background:var(--surface2);flex-shrink:0}
.help-tab{padding:12px 18px;border:none;background:none;font-family:'DM Sans',sans-serif;font-size:13px;font-weight:500;color:var(--text3);cursor:pointer;border-bottom:2px solid transparent;margin-bottom:-2px;transition:.15s;white-space:nowrap}
.help-tab:hover{color:var(--text);background:var(--surface)}
.help-tab.active{color:var(--accent);border-bottom-color:var(--accent);background:var(--surface)}
.help-body{flex:1;overflow-y:auto;padding:28px 32px}
.help-body h2{font-family:'Syne',sans-serif;font-size:20px;font-weight:700;color:var(--text);margin-bottom:16px;padding-bottom:8px;border-bottom:2px solid var(--border)}
.help-body h3{font-size:14px;font-weight:600;color:var(--text);margin:20px 0 8px;display:flex;align-items:center;gap:8px}
.help-body h3::before{content:'';display:inline-block;width:4px;height:14px;background:var(--accent);border-radius:2px;flex-shrink:0}
.help-body p{font-size:13px;color:var(--text2);line-height:1.7;margin-bottom:10px}
.help-body ul{margin:0 0 12px 0;padding-left:20px}
.help-body ul li{font-size:13px;color:var(--text2);line-height:1.7;margin-bottom:4px}
.help-body ul li b{color:var(--text)}
.help-step{display:flex;gap:12px;margin-bottom:14px;align-items:flex-start}
.help-step-num{width:26px;height:26px;border-radius:50%;background:var(--accent);color:#fff;font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px}
.help-step-body{flex:1}
.help-step-body b{font-size:13px;font-weight:600;color:var(--text);display:block;margin-bottom:3px}
.help-step-body p{font-size:12px;color:var(--text3);margin:0;line-height:1.6}
.help-note{background:var(--accent-light);border:1px solid #BFDBFE;border-radius:var(--radius-sm);padding:10px 14px;font-size:12px;color:#1e40af;margin:12px 0}
.help-warn{background:var(--warn-light);border:1px solid #FCD34D;border-radius:var(--radius-sm);padding:10px 14px;font-size:12px;color:#92400E;margin:12px 0}
.help-code{background:var(--surface2);border:1px solid var(--border);border-radius:var(--radius-sm);padding:10px 14px;font-family:'DM Mono',monospace;font-size:12px;color:var(--text);margin:8px 0;line-height:1.6;white-space:pre-wrap}
.help-table{width:100%;border-collapse:collapse;margin:10px 0;font-size:12px}
.help-table th{background:var(--surface2);padding:7px 12px;text-align:left;font-weight:600;color:var(--text3);border:1px solid var(--border)}
.help-table td{padding:7px 12px;border:1px solid var(--border);color:var(--text2);line-height:1.5}
.help-table tr:nth-child(even) td{background:#FAFAF8}

svg.icon-svg{width:14px;height:14px;stroke:currentColor;fill:none;stroke-width:2;stroke-linecap:round;stroke-linejoin:round;flex-shrink:0}
</style>
</head>
<body>

<!-- Header -->
<header class="app-header">
  <div class="app-logo">WBS<span>Manager</span></div>
  <div class="header-divider"></div>
  <!-- Project selector -->
  <div class="proj-selector" title="プロジェクトを切り替え">
    <div class="proj-color-dot" id="header-proj-dot" style="background:#2563EB"></div>
    <select id="header-proj-select" onchange="switchProject(this.value)"></select>
  </div>
  <button class="btn btn-sm" onclick="openNewProjectModal()" title="新規プロジェクト作成" style="padding:5px 8px">
    <svg class="icon-svg" viewBox="0 0 24 24"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg>
  </button>
  <div class="header-divider"></div>
  <div class="header-tabs">
    <button class="tab-btn active" onclick="switchTab('list')">📋 リスト</button>
    <button class="tab-btn" onclick="switchTab('gantt')">📊 ガントチャート</button>
    <button class="tab-btn" id="lightning-btn"
      onclick="toggleLightningLine()"
      title="イナズマ線を表示"
      style="display:none;border:1px solid var(--border);border-radius:var(--radius-sm);background:var(--surface);color:var(--text3);padding:5px 10px;font-size:12px">
      ⚡ イナズマ線
    </button>
    <!-- スケール切替 -->
    <div id="gantt-scale-btns" style="display:none;margin-left:4px;display:none;gap:2px">
      <button class="tab-btn gantt-scale-btn" data-scale="day"     onclick="setGanttScale('day')"     style="padding:5px 8px;font-size:11px">日</button>
      <button class="tab-btn gantt-scale-btn" data-scale="week"    onclick="setGanttScale('week')"    style="padding:5px 8px;font-size:11px">週</button>
      <button class="tab-btn gantt-scale-btn" data-scale="month"   onclick="setGanttScale('month')"   style="padding:5px 8px;font-size:11px">月</button>
      <button class="tab-btn gantt-scale-btn" data-scale="quarter" onclick="setGanttScale('quarter')" style="padding:5px 8px;font-size:11px">四半期</button>
      <button class="tab-btn gantt-scale-btn" data-scale="year"    onclick="setGanttScale('year')"    style="padding:5px 8px;font-size:11px">年</button>
    </div>
  </div>
  <div class="header-spacer"></div>
  <!-- 参照モードバナー（CSVモード時のみ表示） -->
  <div class="readonly-banner" id="readonly-banner">
    <span id="readonly-banner-icon">👁</span>
    <span id="readonly-banner-text">参照モード</span>
  </div>
  <!-- 編集開始/完了ボタン（CSVモード時のみ表示） -->
  <button class="btn btn-sm checkin-btn" id="checkin-btn" style="display:none" onclick="checkin()">✏️ 編集開始</button>
  <button class="btn btn-sm checkout-btn" id="checkout-btn" style="display:none" onclick="checkout()">✅ 編集完了</button>
  <!-- Storage indicator -->
  <div class="storage-indicator mode-ls" id="storage-indicator" onclick="openStorageModal()" title="ストレージ設定">
    <div class="storage-dot" id="storage-dot" style="background:var(--text3)"></div>
    <span id="storage-label">💾 ローカル</span>
  </div>
  <div class="header-actions">
    <button class="btn btn-sm" onclick="exportCSV()">
      <svg class="icon-svg" viewBox="0 0 24 24"><path d="M21 15v4a2 2 0 01-2 2H5a2 2 0 01-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
      エクスポート
    </button>
    <button class="btn btn-sm" onclick="triggerImport()">
      <svg class="icon-svg" viewBox="0 0 24 24"><path d="M21 15v4a2 2 0 01-2 2H5a2 2 0 01-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
      インポート
    </button>
    <input type="file" id="import-file-input" accept=".csv" style="display:none" onchange="importCSV(event)">
    <button class="btn btn-sm" onclick="openHelpModal()" title="操作マニュアル">
      ❓ ヘルプ
    </button>
    <button class="btn btn-primary" onclick="openAddModal(null)">
      <svg class="icon-svg" viewBox="0 0 24 24" style="stroke:#fff"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg>
      タスク追加
    </button>
    <div class="header-divider"></div>
    <!-- User switcher button -->
    <button class="user-btn" id="user-btn" onclick="toggleUserPanel()">
      <div class="avatar-lg" id="header-user-avatar" style="background:#9B9890">?</div>
      <span id="header-user-name">ゲスト</span>
      <span style="color:var(--text3);font-size:10px;margin-left:2px">▾</span>
    </button>
  </div>
</header>

<div class="app-body">
  <!-- Sidebar -->
  <aside class="sidebar" id="sidebar">
    <button class="sidebar-toggle" id="sidebar-toggle" onclick="toggleSidebar()" title="サイドバーを折りたたむ">◀</button>

    <!-- Collapsed mini-view -->
    <div class="sidebar-collapsed-icons">
      <div class="collapsed-stat" title="総タスク数">
        <div class="collapsed-stat-num" id="stat-total-mini">0</div>
        <div class="collapsed-stat-dot" style="background:var(--text3)"></div>
      </div>
      <div class="collapsed-stat" title="完了タスク">
        <div class="collapsed-stat-num" id="stat-done-mini">0</div>
        <div class="collapsed-stat-dot" style="background:var(--success)"></div>
      </div>
      <div class="collapsed-stat" title="期限超過">
        <div class="collapsed-stat-num" id="stat-overdue-mini" style="color:var(--danger)">0</div>
        <div class="collapsed-stat-dot" style="background:var(--danger)"></div>
      </div>
    </div>

    <!-- Full content -->
    <div class="sidebar-content">
      <!-- Project management panel -->
      <div class="sidebar-section" style="margin-top:4px">
        <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:10px">
          <div class="sidebar-label" style="margin-bottom:0">プロジェクト</div>
          <button class="btn btn-sm" onclick="openNewProjectModal()" style="padding:3px 8px;font-size:11px;gap:4px">
            <svg class="icon-svg" viewBox="0 0 24 24" style="width:11px;height:11px"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg>新規
          </button>
        </div>
        <div id="sidebar-proj-list"></div>
      </div>
      <div style="height:1px;background:var(--border);margin:4px 0 16px"></div>
      <div class="sidebar-section">
        <div class="sidebar-label">プロジェクト概要</div>
        <div class="stat-card">
          <div class="stat-num" id="stat-total">0</div>
          <div class="stat-label">総タスク数</div>
        </div>
        <div class="stat-card">
          <div class="stat-num" id="stat-done">0</div>
          <div class="stat-label">完了タスク</div>
          <div class="mini-progress"><div class="mini-fill" id="stat-bar" style="width:0%"></div></div>
        </div>
        <div class="stat-card">
          <div class="stat-num" id="stat-overdue" style="color:var(--danger)">0</div>
          <div class="stat-label">期限超過</div>
        </div>
        <div class="stat-card" id="conflict-stat-card" style="display:none;border:1px solid #FCA5A5;background:#FEF2F2">
          <div class="stat-num" id="stat-conflict" style="color:var(--danger)">0</div>
          <div class="stat-label" style="color:var(--danger)">⚠ フォルダ日程の矛盾</div>
        </div>
      </div>
      <div class="sidebar-section">
        <div class="sidebar-label">ステータス凡例</div>
        <div class="legend-item"><div class="legend-dot" style="background:#9B9890"></div>未着手</div>
        <div class="legend-item"><div class="legend-dot" style="background:var(--warn)"></div>進行中</div>
        <div class="legend-item"><div class="legend-dot" style="background:var(--success)"></div>完了</div>
        <div class="legend-item"><div class="legend-dot" style="background:var(--danger)"></div>ブロック中</div>
      </div>
      <div class="sidebar-section">
        <div class="sidebar-label">関係線</div>
        <div class="legend-item">
          <svg width="28" height="10" style="flex-shrink:0"><line x1="0" y1="5" x2="22" y2="5" stroke="#64748B" stroke-width="1.5" stroke-dasharray="4,2"/><polygon points="22,2 28,5 22,8" fill="#64748B"/></svg>
          通常（順序OK）
        </div>
        <div class="legend-item">
          <svg width="28" height="10" style="flex-shrink:0"><line x1="0" y1="5" x2="22" y2="5" stroke="#DC2626" stroke-width="2" stroke-dasharray="4,2"/><polygon points="22,2 28,5 22,8" fill="#DC2626"/></svg>
          <span style="color:var(--danger)">期間重複（要確認）</span>
        </div>
      </div>
      <div class="sidebar-section">
        <div class="sidebar-label">担当者</div>
        <div id="assignee-legend"></div>
      </div>
    </div><!-- end sidebar-content -->
  </aside>

  <!-- Main -->
  <div class="main-area">
    <!-- Toolbar -->
    <div class="toolbar">
      <div class="search-box">
        <svg class="icon-svg" viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="M21 21l-4.35-4.35"/></svg>
        <input id="search-input" type="text" placeholder="タスクを検索..." oninput="renderAll()">
      </div>
      <select class="filter-select" id="filter-status" onchange="renderAll()">
        <option value="">全ステータス</option>
        <option value="todo">未着手</option>
        <option value="doing">進行中</option>
        <option value="done">完了</option>
        <option value="block">ブロック中</option>
      </select>
      <select class="filter-select" id="filter-assignee" onchange="renderAll()">
        <option value="">全担当者</option>
      </select>
      <button class="btn btn-sm" onclick="expandAll()">全展開</button>
      <button class="btn btn-sm" onclick="collapseAll()">全折りたたみ</button>
      <button class="btn btn-sm sort-toggle-btn" id="sort-toggle-btn" onclick="toggleSortMode()" title="並替モードのON/OFF">
        ⠿ 並替モード
      </button>
      <div id="sort-mode-hint" style="display:none;align-items:center;gap:6px;font-size:11px;color:var(--warn);background:var(--warn-light);border:1px solid var(--warn);border-radius:var(--radius-sm);padding:4px 10px">
        <span>⠿</span>
        <span>並替モードON：左端の <b>⠿</b> をドラッグして順序を変更。上下25%で同列、中央25%で子になります。</span>
      </div>
      <div style="margin-left:auto;font-size:11px;color:var(--text3);display:flex;align-items:center;gap:6px" id="dep-hint">
        <span>💡</span>
        <span>行の <b style="color:var(--accent)">＋子</b> で子タスク追加 ／ <b style="color:var(--text2)">＋同列</b> で同階層追加 ／ 右クリックでメニュー</span>
      </div>
    </div>

    <!-- List View -->
    <div id="list-view" class="wbs-container">
      <table class="wbs-table">
        <thead>
          <tr>
            <th style="width:80px;padding:0 8px"></th>
            <th style="width:60px;text-align:center">No</th>
            <th style="min-width:300px">タスク名 / 成果物</th>
            <th>ステータス</th>
            <th>担当者</th>
            <th>開始日</th>
            <th>終了日</th>
            <th>進捗</th>
            <th>依存関係</th>
          </tr>
        </thead>
        <tbody id="wbs-tbody"></tbody>
      </table>
    </div>

    <!-- Gantt View -->
    <div id="gantt-view" class="gantt-wrapper" style="display:none">
      <div id="gantt-inner"></div>
    </div>
  </div>
</div>

<!-- Detail Panel -->
<div class="detail-panel" id="detail-panel">
  <div class="detail-header">
    <div class="detail-title-wrap">
      <div class="detail-title" id="dp-title">-</div>
      <div class="detail-wbs-id" id="dp-id">-</div>
    </div>
    <button class="detail-close" onclick="closeDetail()">✕</button>
  </div>
  <div class="detail-body">
    <div class="detail-section">
      <div class="detail-section-label">基本情報</div>
      <div class="detail-field"><label>種別</label>
        <select id="dp-type" onchange="dpUpdate('type',this.value)">
          <option value="task">📄 タスク</option>
          <option value="folder">📁 フォルダ（グループ）</option>
        </select>
      </div>
      <div class="detail-field"><label>タスク名</label><input id="dp-name" type="text" oninput="dpUpdate('name',this.value)"></div>
      <div class="detail-field"><label>成果物定義</label><textarea id="dp-deliverable" oninput="dpUpdate('deliverable',this.value)"></textarea></div>
      <div class="detail-field"><label>備考</label><textarea id="dp-note" oninput="dpUpdate('note',this.value)"></textarea></div>
    </div>
    <div class="detail-section">
      <div class="detail-section-label">スケジュール</div>
      <div class="detail-field"><label>開始日</label><input id="dp-start" type="date" oninput="dpUpdate('start',this.value)"></div>
      <div class="detail-field"><label>終了日</label><input id="dp-end" type="date" oninput="dpUpdate('end',this.value)"></div>
      <div class="detail-field">
        <label>担当者</label>
        <select id="dp-assignee-select" style="width:100%;padding:8px 10px;border:1px solid var(--border);border-radius:var(--radius-sm);font-family:'DM Sans',sans-serif;font-size:13px;color:var(--text);background:var(--surface);outline:none;margin-bottom:6px" onchange="onAssigneeSelectChange('dp')">
          <option value="">（未割当）</option>
        </select>
        <input id="dp-assignee" type="text" list="dp-assignee-list" autocomplete="off" placeholder="または直接入力" oninput="onAssigneeInputChange('dp');dpUpdate('assignee',this.value)">
        <datalist id="dp-assignee-list"></datalist>
        <div style="font-size:10px;color:var(--text3);margin-top:3px">ユーザー一覧から選択 または 直接入力</div>
      </div>
    </div>
    <div class="detail-section">
      <div class="detail-section-label">ステータス・進捗</div>
      <div class="detail-field"><label>ステータス</label>
        <select id="dp-status" onchange="dpUpdate('status',this.value)">
          <option value="todo">未着手</option>
          <option value="doing">進行中</option>
          <option value="done">完了</option>
          <option value="block">ブロック中</option>
        </select>
      </div>
      <div class="detail-field"><label>進捗率: <span id="dp-prog-val">0</span>%</label>
        <input id="dp-progress" type="range" min="0" max="100" step="5" oninput="document.getElementById('dp-prog-val').textContent=this.value;dpUpdate('progress',parseInt(this.value))">
      </div>
    </div>
    <div class="detail-section">
      <div class="detail-section-label">依存関係</div>
      <div class="detail-field"><label>前タスクNo (カンマ区切り)</label><input id="dp-deps" type="text" placeholder="例: 1.1, 1.2" oninput="dpUpdateDeps(this.value)"></div>
    </div>
  </div>
  <div class="detail-actions">
    <button class="btn btn-sm" style="color:var(--danger)" onclick="deleteSelectedTask()">🗑 削除</button>
    <div style="flex:1"></div>
    <button class="btn btn-sm btn-primary" onclick="closeDetail()">閉じる</button>
  </div>
</div>

<!-- Add Task Modal -->
<div class="modal-overlay" id="add-modal">
  <div class="modal">
    <div class="modal-title" id="modal-title-text">タスクを追加</div>
    <!-- parent context banner -->
    <div id="modal-parent-banner" style="display:none;margin-bottom:16px;padding:10px 14px;background:var(--accent-light);border:1px solid #BFDBFE;border-radius:var(--radius-sm);font-size:12px;color:var(--accent)">
      <span style="font-weight:600">📂 親タスク：</span><span id="modal-parent-label"></span>
      <div style="margin-top:4px;color:var(--text3);font-size:11px">このタスクは上記の子タスクとして追加されます</div>
    </div>
    <div id="modal-toplevel-banner" style="margin-bottom:16px;padding:10px 14px;background:var(--surface2);border:1px solid var(--border);border-radius:var(--radius-sm);font-size:12px;color:var(--text2)">
      <span style="font-weight:600">📁 最上位タスク</span>
      <div style="margin-top:4px;color:var(--text3);font-size:11px">フェーズや大項目として追加されます</div>
    </div>
    <div class="modal-grid">
      <div class="form-field full"><label>タスク名 *</label><input id="m-name" type="text" placeholder="名前を入力"></div>
      <div class="form-field full"><label>成果物定義</label><textarea id="m-deliverable" placeholder="このタスクの成果物・完了条件を記述"></textarea></div>
      <div class="form-field"><label>種別</label>
        <select id="m-type">
          <option value="task">📄 タスク</option>
          <option value="folder">📁 フォルダ（グループ）</option>
        </select>
      </div>
      <div class="form-field"><label>ステータス</label>
        <select id="m-status">
          <option value="todo">未着手</option>
          <option value="doing">進行中</option>
          <option value="done">完了</option>
          <option value="block">ブロック中</option>
        </select>
      </div>
      <div class="form-field">
        <label>担当者</label>
        <div style="display:flex;gap:8px;align-items:center">
          <select id="m-assignee-select" style="flex:1;padding:8px 10px;border:1px solid var(--border);border-radius:var(--radius-sm);font-family:'DM Sans',sans-serif;font-size:13px;color:var(--text);background:var(--surface);outline:none" onchange="onAssigneeSelectChange('m')">
            <option value="">（未割当）</option>
          </select>
          <input id="m-assignee" type="text" placeholder="または直接入力" list="m-assignee-list" autocomplete="off" style="flex:1;padding:8px 10px;border:1px solid var(--border);border-radius:var(--radius-sm);font-family:'DM Sans',sans-serif;font-size:13px;color:var(--text);background:var(--surface);outline:none" oninput="onAssigneeInputChange('m')">
          <datalist id="m-assignee-list"></datalist>
        </div>
        <div style="font-size:10px;color:var(--text3);margin-top:3px">ユーザー一覧から選択 または 直接入力</div>
      </div>
      <div class="form-field"><label>開始日</label><input id="m-start" type="date"></div>
      <div class="form-field"><label>終了日</label><input id="m-end" type="date"></div>
      <div class="form-field"><label>進捗率</label><input id="m-progress" type="number" min="0" max="100" value="0" placeholder="0"></div>
      <div class="form-field"><label>依存タスクID</label><input id="m-deps" type="text" placeholder="例: 1.1, 1.2"></div>
      <div class="form-field full" id="modal-parent-field">
        <label>親タスク <span style="font-weight:400;color:var(--text3)">（変更可）</span></label>
        <select id="m-parent"><option value="">なし（最上位）</option></select>
      </div>
      <div class="form-field full"><label>備考</label><textarea id="m-note" placeholder="メモ・補足情報"></textarea></div>
    </div>
    <div class="modal-footer">
      <button class="btn" onclick="closeAddModal()">キャンセル</button>
      <button class="btn btn-primary" onclick="submitAddTask()">追加</button>
    </div>
  </div>
</div>

<!-- ═══ User switcher panel ═══ -->
<div class="user-panel" id="user-panel">
  <div class="user-panel-header">
    <span class="user-panel-title">ユーザー切替</span>
    <button class="btn btn-sm" onclick="openUserMgmtModal()" style="padding:3px 8px;font-size:11px">管理</button>
  </div>
  <div class="user-list" id="user-list"></div>
  <div class="user-panel-footer">
    <button class="btn btn-sm" onclick="openAddUserModal()" style="flex:1;justify-content:center">
      <svg class="icon-svg" viewBox="0 0 24 24"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg>
      新規ユーザー追加
    </button>
  </div>
</div>

<!-- ═══ Add / Edit user modal ═══ -->
<div class="modal-overlay z-top" id="user-edit-modal">
  <div class="modal" style="max-width:440px">
    <div class="modal-title" id="user-edit-title">ユーザーを追加</div>
    <input type="hidden" id="ue-id">
    <div class="user-grid">
      <div class="form-field full">
        <label>氏名 *</label>
        <input id="ue-name" type="text" placeholder="例: 田中 太郎">
      </div>
      <div class="form-field full">
        <label>役割 / 所属</label>
        <input id="ue-role" type="text" placeholder="例: バックエンドエンジニア">
      </div>
      <div class="form-field full">
        <label>メモ</label>
        <textarea id="ue-note" placeholder="連絡先・備考など" style="min-height:52px"></textarea>
      </div>
      <div class="form-field full">
        <label>アバターカラー</label>
        <div id="ue-color-picker" style="display:flex;gap:8px;flex-wrap:wrap;margin-top:6px"></div>
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn" onclick="closeUserEditModal()">キャンセル</button>
      <button class="btn btn-primary" onclick="submitUserEdit()">保存</button>
    </div>
  </div>
</div>

<!-- ═══ User management modal ═══ -->
<div class="modal-overlay" id="user-mgmt-modal">
  <div class="modal" style="max-width:520px">
    <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:20px">
      <div class="modal-title" style="margin:0">ユーザー管理</div>
      <button class="btn btn-sm btn-primary" onclick="openAddUserModal()">
        <svg class="icon-svg" viewBox="0 0 24 24" style="stroke:#fff"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg>
        追加
      </button>
    </div>
    <div id="user-mgmt-list" style="display:flex;flex-direction:column;gap:8px;max-height:400px;overflow-y:auto"></div>
    <div class="modal-footer" style="margin-top:20px">
      <button class="btn btn-primary" onclick="closeUserMgmtModal()">閉じる</button>
    </div>
  </div>
</div>

<!-- ═══ Login screen ═══ -->
<div class="login-screen" id="login-screen">
  <div class="login-card">
    <div class="login-logo">WBS<span>Manager</span></div>
    <!-- CSV再接続バナー（CSVモード時のみ表示） -->
    <div id="login-csv-banner" style="display:none;margin-bottom:20px;padding:12px 14px;background:#ECFDF5;border:1px solid #6EE7B7;border-radius:var(--radius);font-size:12px;color:#065F46">
      <div style="font-weight:600;margin-bottom:6px">☁️ OneDriveモードが有効です</div>
      <div id="login-csv-desc" style="color:#047857;margin-bottom:10px">前回使用したフォルダに再接続してデータを読み込みます。</div>
      <!-- ワンクリック再接続ボタン（IDBにハンドルがある場合） -->
      <button id="login-quick-reconnect-btn" class="btn btn-sm" onclick="quickReconnect()" style="display:none;background:#059669;color:#fff;border-color:#059669;width:100%;justify-content:center;margin-bottom:6px">
        ⚡ ワンクリックで再接続（前回のフォルダ）
      </button>
      <!-- 通常の再選択ボタン -->
      <button class="btn btn-sm" onclick="reconnectCsvAndLogin()" style="background:#047857;color:#fff;border-color:#047857;width:100%;justify-content:center">
        📂 フォルダを選択して接続
      </button>
      <div style="margin-top:8px;font-size:11px;color:#6EE7B7;text-align:center">または下のユーザーを選択してlocalStorageのデータで続行</div>
    </div>
    <div class="login-sub">ログインするユーザーを選択してください</div>
    <div class="login-user-grid" id="login-user-grid"></div>
    <button class="btn" style="width:100%;justify-content:center" onclick="openAddUserModal(true)">
      <svg class="icon-svg" viewBox="0 0 24 24"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg>
      新しいユーザーを追加してログイン
    </button>
  </div>
</div>

<!-- ═══ Storage settings modal ═══ -->
<div class="modal-overlay" id="storage-modal">
  <div class="modal" style="max-width:480px">
    <div class="modal-title">ストレージ設定</div>
    <p style="font-size:12px;color:var(--text3);margin-bottom:16px">データの保存先を選択します。切り替え時は現在のデータを引き継ぎます。</p>

    <!-- Option 1: localStorage -->
    <div class="storage-option selected" id="storage-opt-ls" onclick="selectStorageOption('localStorage')">
      <div class="storage-option-icon">💾</div>
      <div>
        <div class="storage-option-title">ローカルストレージ（デフォルト）</div>
        <div class="storage-option-desc">ブラウザに内蔵されたストレージに保存します。<br>設定不要ですぐ使えます。ブラウザやPCをまたいだ共有はできません。</div>
      </div>
    </div>

<!-- Option 2: OneDrive -->
    <div class="storage-option" id="storage-opt-csv" onclick="selectStorageOption('csvFile')">
      <div class="storage-option-icon">☁️</div>
      <div>
        <div class="storage-option-title">OneDrive（フォルダ指定）</div>
        <div class="storage-option-desc">OneDriveの同期フォルダに <code>wbs_data.json</code> を自動保存します。<br>SharePoint同期フォルダを指定すればチーム間での共有が可能です。<br><b>※ Chrome / Edge のみ対応</b></div>
      </div>
    </div>

    <!-- CSV/OneDrive mode detail -->
    <div id="storage-csv-detail" style="display:none;margin-top:12px;padding:14px;background:var(--surface2);border-radius:var(--radius);border:1px solid var(--border)">
      <div style="font-size:12px;font-weight:600;margin-bottom:10px;color:var(--text2)">☁️ OneDrive フォルダ設定</div>
      <div id="storage-csv-folder-info" style="font-size:12px;color:var(--text3);margin-bottom:10px">フォルダが選択されていません</div>
      <button class="btn btn-sm" onclick="selectCsvFolder()" id="storage-select-folder-btn">
        📂 OneDriveフォルダを選択
      </button>
      <div style="margin-top:12px;font-size:11px;color:var(--text3)">
        <b>保存ファイル：</b><br>
        　<code>wbs_data.json</code> — 全プロジェクトデータ<br>
        　<code>wbs_lock.json</code> — 編集中ユーザー情報（参考表示用）
      </div>
    </div>

    <!-- Lock status -->
    <div id="storage-lock-info" style="display:none;margin-top:10px;padding:10px 14px;background:var(--warn-light);border:1px solid var(--warn);border-radius:var(--radius-sm);font-size:12px;color:var(--warn)"></div>

    <!-- Reset to sample -->
    <div style="margin-top:14px;padding-top:14px;border-top:1px solid var(--border)">
      <div style="font-size:11px;color:var(--text3);margin-bottom:8px">⚠ データのリセット</div>
      <button class="btn btn-sm" onclick="resetToSampleData()" style="color:var(--danger);border-color:var(--danger)">
        🔄 サンプルデータでリセット（全データ削除）
      </button>
    </div>

    <div class="modal-footer">
      <button class="btn" onclick="closeStorageModal()">キャンセル</button>
      <button class="btn btn-primary" id="storage-apply-btn" onclick="applyStorageMode()">適用</button>
    </div>
  </div>
</div>

<!-- ═══ Help Modal ═══ -->
<div class="modal-overlay" id="help-modal">
  <div class="modal help-modal">
    <!-- タブナビ -->
    <div class="help-tabs">
      <button class="help-tab active" onclick="switchHelpTab('prepare')">📋 事前準備</button>
      <button class="help-tab" onclick="switchHelpTab('basic')">🚀 基本操作</button>
      <button class="help-tab" onclick="switchHelpTab('gantt')">📊 ガントチャート</button>
      <button class="help-tab" onclick="switchHelpTab('share')">☁️ OneDrive共有</button>
      <button class="help-tab" onclick="switchHelpTab('tips')">💡 Tips</button>
      <div style="flex:1"></div>
      <button onclick="closeHelpModal()" style="border:none;background:none;cursor:pointer;font-size:18px;color:var(--text3);padding:0 16px">✕</button>
    </div>

    <!-- ── 事前準備 ── -->
    <div class="help-body" id="help-tab-prepare">
      <h2>📋 事前準備</h2>

      <h3>推奨ブラウザ</h3>
      <p>WBS ManagerはChrome または Edge での利用を推奨します。OneDrive連携（File System Access API）はSafariでは動作しません。</p>

      <h3>OneDrive共有を使う場合の事前準備</h3>
      <p>複数人でプロジェクトデータを共有するには、SharePointのフォルダをOneDriveにショートカット追加する方法が最も簡単です。</p>

      <div class="help-step">
        <div class="help-step-num">1</div>
        <div class="help-step-body">
          <b>SharePointサイトを開く</b>
          <p>ブラウザでSharePointの対象サイトにアクセスします。<br>例：<code>https://会社名.sharepoint.com/sites/プロジェクト名</code></p>
        </div>
      </div>
      <div class="help-step">
        <div class="help-step-num">2</div>
        <div class="help-step-body">
          <b>ドキュメントライブラリのフォルダを選択する</b>
          <p>左メニューの「ドキュメント」または任意のライブラリを開き、WBSデータを置きたいフォルダに移動します。新しいフォルダを作成する場合は「＋ 新規」→「フォルダー」から作成します（例：<code>WBSData</code>）。</p>
        </div>
      </div>
      <div class="help-step">
        <div class="help-step-num">3</div>
        <div class="help-step-body">
          <b>「OneDriveへのショートカットを追加」をクリック</b>
          <p>フォルダを右クリック → 「OneDriveへのショートカットを追加」を選択します。または上部メニューの「☁ OneDriveへのショートカットを追加」ボタンをクリックします。</p>
        </div>
      </div>
      <div class="help-step">
        <div class="help-step-num">4</div>
        <div class="help-step-body">
          <b>OneDriveデスクトップアプリで同期を確認する</b>
          <p>タスクバーのOneDriveアイコン（雲マーク）をクリックし、同期が完了しているか確認します。エクスプローラーを開き、OneDriveフォルダ内にSharePointのフォルダが表示されれば成功です。</p>
        </div>
      </div>
      <div class="help-step">
        <div class="help-step-num">5</div>
        <div class="help-step-body">
          <b>チームメンバー全員が同じ手順を実施する</b>
          <p>共有したいメンバー全員がSharePointフォルダへのアクセス権限を持ち、同じ手順でOneDriveにショートカットを追加します。これにより全員のPCに同じフォルダが同期されます。</p>
        </div>
      </div>

      <div class="help-note">💡 OneDriveデスクトップアプリがインストールされていない場合は、Microsoft公式サイトからダウンロードしてサインインしてください。会社のMicrosoft 365アカウントでサインインします。</div>

      <h3>WBS Managerのセットアップ</h3>
      <div class="help-step">
        <div class="help-step-num">1</div>
        <div class="help-step-body">
          <b>HTMLファイルをデスクトップに保存する</b>
          <p><code>wbs-tool.html</code> をデスクトップまたは任意のフォルダに保存し、Chrome または Edge でダブルクリックして開きます。</p>
        </div>
      </div>
      <div class="help-step">
        <div class="help-step-num">2</div>
        <div class="help-step-body">
          <b>ユーザー登録を行う</b>
          <p>初回起動時はサンプルユーザーで自動ログインされます。右上のユーザーアイコン → 「管理」からメンバー全員のユーザーを登録しておくと便利です。</p>
        </div>
      </div>
      <div class="help-step">
        <div class="help-step-num">3</div>
        <div class="help-step-body">
          <b>ストレージをOneDriveに切り替える</b>
          <p>ヘッダーの「💾 ローカル」→「☁️ OneDrive（フォルダ指定）」を選択 → 「📂 OneDriveフォルダを選択」で手順4で同期したフォルダを指定します。</p>
        </div>
      </div>
    </div>

    <!-- ── 基本操作 ── -->
    <div class="help-body" id="help-tab-basic" style="display:none">
      <h2>🚀 基本操作</h2>

      <h3>タスク・フォルダの追加</h3>
      <table class="help-table">
        <tr><th>操作</th><th>方法</th></tr>
        <tr><td>最上位タスクを追加</td><td>ヘッダーの「＋ タスク追加」ボタン</td></tr>
        <tr><td>同じ階層に追加</td><td>行の「＋同列」ボタン</td></tr>
        <tr><td>子タスクを追加</td><td>行の「＋子」ボタン（青色）</td></tr>
        <tr><td>コンテキストメニュー</td><td>行を右クリック</td></tr>
      </table>

      <h3>フォルダとタスクの違い</h3>
      <ul>
        <li><b>📁 フォルダ</b>：グループ（フェーズ）を表します。進捗率は子タスクから自動計算されます。</li>
        <li><b>📄 タスク</b>：実際の作業単位です。進捗率を手動で入力します。</li>
      </ul>
      <p>タスク追加モーダルの「種別」で選択できます。後から詳細パネルで変更も可能です。</p>

      <h3>並び替え</h3>
      <p>ツールバーの「⠿ 並替モード」をONにすると、行左端の <b>⠿</b> ハンドルをドラッグして順序を変更できます。ターゲット行の上25%にドロップすると同列の上に、下25%では同列の下に、中央50%では子として挿入されます。</p>

      <h3>依存関係の設定</h3>
      <ul>
        <li>リストビューで行をドラッグ → 別の行にドロップ（並替モードOFF時）</li>
        <li>詳細パネルの「前タスクNo」に番号をカンマ区切りで入力</li>
        <li>同じ依存をもう一度ドロップすると削除できます</li>
      </ul>

      <h3>CSV インポート / エクスポート</h3>
      <ul>
        <li><b>エクスポート</b>：「エクスポート」ボタンでCSVを保存。内部ID・No・依存関係（ID/No両方）が含まれます。</li>
        <li><b>インポート</b>：「インポート」ボタンでCSVを選択。内部IDがあればアップサート（部分更新）または上書きを選択できます。</li>
      </ul>
    </div>

    <!-- ── ガントチャート ── -->
    <div class="help-body" id="help-tab-gantt" style="display:none">
      <h2>📊 ガントチャート</h2>

      <h3>表示スケールの切替</h3>
      <table class="help-table">
        <tr><th>ボタン</th><th>単位</th><th>用途</th></tr>
        <tr><td>日</td><td>1日単位</td><td>直近の詳細スケジュール確認</td></tr>
        <tr><td>週</td><td>1週単位</td><td>月次の進捗管理</td></tr>
        <tr><td>月</td><td>1ヶ月単位</td><td>フェーズ全体の把握</td></tr>
        <tr><td>四半期</td><td>3ヶ月単位</td><td>年間計画の確認</td></tr>
        <tr><td>年</td><td>1年単位</td><td>複数年プロジェクトの俯瞰</td></tr>
      </table>
      <p>ガントチャートを開くと自動的にTodayが画面中央に表示されます。</p>

      <h3>バーの操作</h3>
      <ul>
        <li><b>バー中央をドラッグ</b>：開始日・終了日を同時にシフト</li>
        <li><b>バー左端をドラッグ</b>：開始日のみ変更</li>
        <li><b>バー右端をドラッグ</b>：終了日のみ変更</li>
      </ul>

      <h3>依存関係の矢印</h3>
      <ul>
        <li><b>グレー点線</b>：正常な依存関係（前工程終了後に後工程が開始）</li>
        <li><b>赤い点線</b>：期間重複あり（前工程終了前に後工程が開始）</li>
      </ul>

      <h3>イナズマ線</h3>
      <p>「⚡ イナズマ線」ボタンで表示/非表示を切り替えます。今日時点で期間が進行中のタスクの実績進捗点を縦につなぎ、遅れ・進みを視覚化します。</p>
      <ul>
        <li><b>🔵 青（今日ラインより右）</b>：進んでいる</li>
        <li><b>🔴 赤（今日ラインより左）</b>：遅れている</li>
        <li><b>◆ 菱形</b>：始点・終点（今日ライン上）または期間超過の遅延タスク</li>
      </ul>
    </div>

    <!-- ── OneDrive共有 ── -->
    <div class="help-body" id="help-tab-share" style="display:none">
      <h2>☁️ OneDrive共有モード</h2>

      <h3>ストレージモードの切替</h3>
      <p>ヘッダーのストレージインジケーター（「💾 ローカル」または「☁️ フォルダ名」）をクリックするとストレージ設定モーダルが開きます。</p>
      <table class="help-table">
        <tr><th>モード</th><th>説明</th></tr>
        <tr><td>💾 ローカルストレージ</td><td>ブラウザに保存。共有不可。設定不要。</td></tr>
        <tr><td>☁️ OneDrive</td><td>OneDrive同期フォルダに保存。複数人で共有可能。</td></tr>
      </table>

      <h3>初回接続の手順</h3>
      <div class="help-step">
        <div class="help-step-num">1</div>
        <div class="help-step-body">
          <b>ストレージ設定を開く</b>
          <p>ヘッダーの「💾 ローカル」をクリック → 「☁️ OneDrive」を選択</p>
        </div>
      </div>
      <div class="help-step">
        <div class="help-step-num">2</div>
        <div class="help-step-body">
          <b>OneDriveフォルダを選択する</b>
          <p>「📂 OneDriveフォルダを選択」をクリック → エクスプローラーが開く → SharePointと同期したフォルダ（例：<code>OneDrive - 会社名 &gt; WBSData</code>）を選択して「フォルダーの選択」をクリック</p>
        </div>
      </div>
      <div class="help-step">
        <div class="help-step-num">3</div>
        <div class="help-step-body">
          <b>「適用」をクリック</b>
          <p>既存データがあれば読み込むか上書きするかを選択します。</p>
        </div>
      </div>

      <h3>2回目以降の起動（ワンクリック再接続）</h3>
      <p>2回目以降はログイン画面に「⚡ ワンクリックで再接続」ボタンが表示されます。クリックするとブラウザの許可ダイアログが出るので「許可」を押すだけで自動接続されます。エクスプローラーは開きません。</p>

      <h3>編集モードと参照モード</h3>
      <div class="help-warn">⚠ OneDriveモードでは起動直後は「参照モード」です。編集するには必ず「✏️ 編集開始」を押してください。</div>
      <table class="help-table">
        <tr><th>状態</th><th>バナー表示</th><th>編集</th></tr>
        <tr><td>参照モード（起動直後）</td><td>👁 参照モード（黄）</td><td>不可</td></tr>
        <tr><td>他ユーザー編集中</td><td>🔒 ○○が編集中（赤）</td><td>不可</td></tr>
        <tr><td>編集モード</td><td>なし</td><td>可能</td></tr>
      </table>
      <ul>
        <li><b>✏️ 編集開始</b>：最新データを読み込み、ロックを取得して編集可能になります</li>
        <li><b>✅ 編集完了</b>：データを保存し、ロックを解放します。必ず押してから離席してください</li>
      </ul>
      <p>ポーリング（30秒ごと）で他ユーザーの編集状態とデータ更新を自動確認します。参照モード中にデータが更新された場合は自動リロードされます。</p>
    </div>

    <!-- ── Tips ── -->
    <div class="help-body" id="help-tab-tips" style="display:none">
      <h2>💡 Tips</h2>

      <h3>フォルダ日程の矛盾を検知</h3>
      <p>子タスクの日程がフォルダの期間を超えている場合、リストとガントチャートの両方で <b style="color:var(--danger)">⚠</b> マークが表示されます。サイドバーにも矛盾件数が表示されます。</p>

      <h3>フォルダの進捗率は自動計算</h3>
      <p>フォルダの進捗率は子タスクの期間で重み付けした加重平均で自動計算されます。手動入力は不要です。</p>

      <h3>サイドバーの折りたたみ</h3>
      <p>サイドバー右上の「◀」ボタンで折りたたむと画面を広く使えます。折りたたみ中も総タスク数・完了数・期限超過数はミニ表示で確認できます。</p>

      <h3>キーボードショートカット</h3>
      <table class="help-table">
        <tr><th>キー</th><th>動作</th></tr>
        <tr><td>Esc</td><td>モーダル・コンテキストメニューを閉じる</td></tr>
        <tr><td>右クリック</td><td>タスク行のコンテキストメニュー（追加・編集・削除）</td></tr>
      </table>

      <h3>CSVエクスポート形式</h3>
      <div class="help-code">ID, No, タスク名, 種別, 成果物, ステータス, 担当者,
開始日, 終了日, 進捗率, 依存関係（ID）, 依存関係（No）, 親ID, 備考</div>
      <p>内部IDが含まれるため、エクスポート→編集→インポートでもアップサートによる部分更新が可能です。</p>

      <h3>データのリセット</h3>
      <p>ストレージ設定モーダル下部の「🔄 サンプルデータでリセット」でデータを初期状態に戻せます。</p>
    </div>
  </div>
</div>

<!-- New Project Modal -->
<div class="modal-overlay" id="new-proj-modal">
  <div class="modal" style="max-width:420px">
    <div class="modal-title">新規プロジェクト</div>
    <div style="display:flex;flex-direction:column;gap:14px">
      <div class="form-field">
        <label>プロジェクト名 *</label>
        <input id="np-name" type="text" placeholder="例: ECサイトリニューアル">
      </div>
      <div class="form-field">
        <label>説明</label>
        <textarea id="np-desc" placeholder="プロジェクトの概要・目的" style="min-height:60px"></textarea>
      </div>
      <div class="form-field">
        <label>カラー</label>
        <div id="np-color-picker" style="display:flex;gap:8px;flex-wrap:wrap;margin-top:4px"></div>
      </div>
      <div class="form-field">
        <label>テンプレート</label>
        <select id="np-template">
          <option value="blank">空白（タスクなし）</option>
          <option value="basic">基本WBSテンプレート（要件定義〜リリース）</option>
        </select>
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn" onclick="closeNewProjectModal()">キャンセル</button>
      <button class="btn btn-primary" onclick="submitNewProject()">作成</button>
    </div>
  </div>
</div>

<!-- Context Menu -->
<div id="ctx-menu" style="display:none;position:fixed;z-index:1000;background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);box-shadow:var(--shadow-md);min-width:200px;overflow:hidden">
  <div id="ctx-header" style="padding:8px 14px;background:var(--surface2);border-bottom:1px solid var(--border);font-size:11px;font-weight:600;color:var(--text3)"></div>
  <button class="ctx-item" id="ctx-add-sibling" onclick="ctxAddSibling()">
    <span style="font-size:14px">➕</span> 同じ階層にタスクを追加
    <span class="ctx-hint">同列</span>
  </button>
  <button class="ctx-item" id="ctx-add-child" onclick="ctxAddChild()">
    <span style="font-size:14px">📂</span> 子タスクを追加
    <span class="ctx-hint">1段下</span>
  </button>
  <div style="height:1px;background:var(--border);margin:4px 0"></div>
  <button class="ctx-item" onclick="ctxEdit()">
    <span style="font-size:14px">✏️</span> 詳細を編集
  </button>
  <button class="ctx-item" style="color:var(--danger)" onclick="ctxDelete()">
    <span style="font-size:14px">🗑</span> 削除
  </button>
</div>

<script>
// ═══════════════════════════════════════════════════
// MULTI-PROJECT DATA MODEL
//  projects : [{id, name, desc, color, uidCounter, tasks:[]}]
//  currentProjectId : string
//  tasks : reference to currentProject.tasks (for compat)
// ═══════════════════════════════════════════════════

const PROJ_COLORS=['#2563EB','#7C3AED','#059669','#D97706','#DC2626','#0891B2','#65A30D','#DB2777','#7C3AED','#374151'];
let _projUid=1;
const projUid=()=>'p'+(_projUid++);

const SAMPLE_TASKS=()=>{
  let u=100;const id=()=>'t'+(u++);
  const t1=id(),t2=id(),t3=id(),t4=id(),t5=id(),t6=id(),t7=id(),t8=id(),t9=id(),t10=id(),t11=id(),t12=id(),t13=id(),t14=id(),t15=id(),t16=id(),t17=id();
  return [
    {id:t1,  parentId:null, type:'folder',name:'フェーズ1: 要件定義',      deliverable:'要件定義書（確定版）',  status:'done',  assignee:'田中 太郎',start:'2026-04-01',end:'2026-04-15',progress:100,deps:[],note:''},
    {id:t2,  parentId:t1,   type:'task',  name:'ビジネス要件整理',          deliverable:'ビジネス要件一覧',       status:'done',  assignee:'田中 太郎',start:'2026-04-01',end:'2026-04-05',progress:100,deps:[],note:''},
    {id:t3,  parentId:t1,   type:'task',  name:'システム要件定義',           deliverable:'システム要件仕様書',      status:'done',  assignee:'佐藤 花子',start:'2026-04-06',end:'2026-04-12',progress:100,deps:[t2],note:''},
    {id:t4,  parentId:t1,   type:'task',  name:'要件レビュー・承認',         deliverable:'承認済み要件書',          status:'done',  assignee:'田中 太郎',start:'2026-04-13',end:'2026-04-15',progress:100,deps:[t3],note:''},
    {id:t5,  parentId:null, type:'folder',name:'フェーズ2: 設計',           deliverable:'設計書一式',              status:'done',  assignee:'佐藤 花子',start:'2026-04-16',end:'2026-05-09',progress:100, deps:[t1],note:''},
    {id:t6,  parentId:t5,   type:'task',  name:'アーキテクチャ設計',         deliverable:'アーキテクチャ設計書',    status:'done',  assignee:'鈴木 一郎',start:'2026-04-16',end:'2026-04-23',progress:100,deps:[t4],note:''},
    {id:t7,  parentId:t5,   type:'task',  name:'DB設計',                    deliverable:'ER図・テーブル定義書',    status:'done',  assignee:'佐藤 花子',start:'2026-04-21',end:'2026-04-30',progress:100, deps:[t6],note:''},
    {id:t8,  parentId:t5,   type:'folder',name:'UI/UXデザイン',             deliverable:'画面設計書',              status:'done',  assignee:'山田 美咲',start:'2026-04-21',end:'2026-05-09',progress:100, deps:[t6],note:''},
    {id:t9,  parentId:t8,   type:'task',  name:'ワイヤーフレーム作成',       deliverable:'全画面ワイヤーフレーム',  status:'done',  assignee:'山田 美咲',start:'2026-04-21',end:'2026-04-28',progress:100,deps:[],note:''},
    {id:t10, parentId:t8,   type:'task',  name:'ビジュアルデザイン',         deliverable:'デザインカンプ',          status:'done',  assignee:'山田 美咲',start:'2026-04-29',end:'2026-05-09',progress:100, deps:[t9],note:''},
    {id:t11, parentId:null, type:'folder',name:'フェーズ3: 開発',           deliverable:'動作するシステム',        status:'doing', assignee:'鈴木 一郎',start:'2026-05-12',end:'2026-06-27',progress:40,  deps:[t5],note:''},
    {id:t12, parentId:t11,  type:'task',  name:'バックエンド開発',           deliverable:'API実装・単体テスト完了', status:'done',  assignee:'鈴木 一郎',start:'2026-05-12',end:'2026-06-06',progress:100,  deps:[t7],note:''},
    {id:t13, parentId:t11,  type:'task',  name:'フロントエンド開発',         deliverable:'画面実装・単体テスト完了',status:'doing', assignee:'田中 太郎',start:'2026-05-19',end:'2026-06-13',progress:55,  deps:[t8,t12],note:''},
    {id:t14, parentId:t11,  type:'task',  name:'結合テスト',                deliverable:'結合テスト報告書',        status:'todo',  assignee:'佐藤 花子',start:'2026-06-16',end:'2026-06-27',progress:0,   deps:[t12,t13],note:''},
    {id:t15, parentId:null, type:'folder',name:'フェーズ4: リリース',        deliverable:'本番リリース完了',        status:'todo',  assignee:'田中 太郎',start:'2026-06-30',end:'2026-07-11',progress:0,   deps:[t11],note:''},
    {id:t16, parentId:t15,  type:'task',  name:'ユーザー受入テスト',         deliverable:'UAT完了報告書',           status:'todo',  assignee:'山田 美咲',start:'2026-06-30',end:'2026-07-07',progress:0,   deps:[t14],note:''},
    {id:t17, parentId:t15,  type:'task',  name:'本番リリース',               deliverable:'リリースノート・展開完了', status:'todo',  assignee:'鈴木 一郎',start:'2026-07-08',end:'2026-07-11',progress:0,   deps:[t16],note:''},
  ];
};

// ════════════════════════════════════════════════════
// STORAGE MODE MANAGEMENT
//  storageMode : 'localStorage' | 'csvFile'
//  csvDirHandle : FileSystemDirectoryHandle | null
// ════════════════════════════════════════════════════
// STORAGE MODE MANAGEMENT
//  storageMode : 'localStorage' | 'csvFile'
//  csvDirHandle : FileSystemDirectoryHandle | null
//
//  設計：
//   - localStorage は常にキャッシュとして書き込む
//   - csvFile モード時は CSV を正とし LS はフォールバック
//   - 起動時：LS から読む → CSVモードなら再接続を促す
//   - 再接続後：CSV から読み直して LS キャッシュも更新
// ════════════════════════════════════════════════════
let storageMode = 'localStorage';
let csvDirHandle = null;
let _selectedStorageOption = 'localStorage';
const CSV_STORAGE_META_KEY = 'wbs_storage_mode_v1';
const LS_KEY = 'wbs_manager_v1';

// ── メタ情報（モード設定）の保存・読み込み ──
function saveStorageMeta(){
  try{
    localStorage.setItem(CSV_STORAGE_META_KEY, JSON.stringify({
      storageMode,
      csvDirName: csvDirHandle ? csvDirHandle.name : null,
      // File System Access APIのハンドル自体は保存不可だがフォルダ名を記憶
      csvDirNameHint: csvDirHandle ? csvDirHandle.name : (
        JSON.parse(localStorage.getItem(CSV_STORAGE_META_KEY)||'{}').csvDirNameHint || null
      )
    }));
  }catch(e){}
}
function loadStorageMeta(){
  try{
    const raw = localStorage.getItem(CSV_STORAGE_META_KEY);
    if(!raw) return;
    const d = JSON.parse(raw);
    storageMode = d.storageMode || 'localStorage';
    // フォルダ名ヒントを返す（UI表示用）
    return d;
  }catch(e){ return null; }
}
function getSavedCsvDirName(){
  try{
    const d=JSON.parse(localStorage.getItem(CSV_STORAGE_META_KEY)||'{}');
    return d.csvDirNameHint||null;
  }catch(e){return null;}
}

// ── インジケーター更新 ──
function updateStorageIndicator(){
  const el  = document.getElementById('storage-indicator');
  const dot = document.getElementById('storage-dot');
  const label = document.getElementById('storage-label');
  if(!el) return;
  if(storageMode==='csvFile'&&csvDirHandle){
    el.className='storage-indicator mode-csv';
    dot.style.background='#059669';
    label.textContent='☁️ '+csvDirHandle.name;
  } else if(storageMode==='csvFile'&&!csvDirHandle){
    el.className='storage-indicator mode-error';
    dot.style.background='#DC2626';
    label.textContent='☁️ 再接続待ち';
  } else {
    el.className='storage-indicator mode-ls';
    dot.style.background='#9B9890';
    label.textContent='💾 ローカル';
  }
}

// ── localStorageからの読み込み ──
function loadFromLS(){
  try{
    const raw = localStorage.getItem(LS_KEY);
    if(!raw) return false;
    const d = JSON.parse(raw);
    if(!d.projects||!d.projects.length) return false;
    applyLoadedData(d);
    return true;
  }catch(e){
    // 破損データをクリア
    try{ localStorage.removeItem(LS_KEY); }catch(e2){}
    return false;
  }
}

// ── 読み込んだデータを変数に反映（共通処理） ──
function applyLoadedData(d){
  projects = d.projects;
  currentProjectId = d.currentProjectId || projects[0].id;
  if(d._projUid) _projUid = d._projUid;
  if(d._uid)     _uid     = d._uid;
  if(d.users && d.users.length){
    users = d.users;
    currentUserId = d.currentUserId || null;
    // userUidカウンターを既存IDより大きい値に設定（衝突防止）
    const maxUid = d.users.reduce((max,u)=>{
      const n=parseInt((u.id||'').replace('u',''))||0;
      return n>max?n:max;
    },0);
    if(maxUid >= _userUid) _userUid = maxUid+1;
  }
}

// ── CSVへの書き込み ──
async function saveToCsvDir(data){
  if(!csvDirHandle) return;
  try{
    const fh = await csvDirHandle.getFileHandle('wbs_data.json', {create:true});
    const w  = await fh.createWritable();
    await w.write(JSON.stringify(data, null, 2));
    await w.close();
    // ロックファイル更新
    const cu = currentUser();
    const lock = {
      lockedBy: cu ? cu.name : 'Unknown',
      userId: currentUserId,
      lockedAt: new Date().toISOString(),
      expires: new Date(Date.now() + 3600000).toISOString()
    };
    const lh = await csvDirHandle.getFileHandle('wbs_lock.json', {create:true});
    const lw = await lh.createWritable();
    await lw.write(JSON.stringify(lock, null, 2));
    await lw.close();
  }catch(e){ console.warn('CSV save failed:', e); }
}

// ── CSVからの読み込み ──
async function loadFromCsvDir(){
  if(!csvDirHandle) return false;
  try{
    const fh   = await csvDirHandle.getFileHandle('wbs_data.json');
    const file = await fh.getFile();
    const text = await file.text();
    const d    = JSON.parse(text);
    if(!d.projects||!d.projects.length) return false;
    applyLoadedData(d);
    // LSキャッシュも更新
    try{ localStorage.setItem(LS_KEY, JSON.stringify(d)); }catch(e){}
    return true;
  }catch(e){ return false; }
}

// ── ロックファイルの確認 ──
async function checkLockFile(){
  if(!csvDirHandle) return null;
  try{
    const lh=await csvDirHandle.getFileHandle('wbs_lock.json');
    const file=await lh.getFile();
    const text=await file.text();
    const lock=JSON.parse(text);
    if(!lock.locked) return null;
    if(lock.expires&&new Date(lock.expires)<new Date()) return null;
    if(lock.userId===currentUserId) return null;
    return lock;
  }catch(e){ return null; }
}

function updateLoginCsvBanner(){
  const banner=document.getElementById('login-csv-banner');
  if(!banner) return;
  if(storageMode==='csvFile'){
    banner.style.display='block';
    const savedName=getSavedCsvDirName();
    const descEl=document.getElementById('login-csv-desc');
    const quickBtn=document.getElementById('login-quick-reconnect-btn');
    if(csvDirHandle){
      // IDBからハンドル復元済み → ワンクリックボタンを表示
      if(descEl) descEl.textContent='「'+(csvDirHandle.name||savedName||'OneDriveフォルダ')+'」にワンクリックで再接続できます。';
      if(quickBtn) quickBtn.style.display='flex';
    } else {
      if(descEl) descEl.textContent=(savedName?'前回のフォルダ「'+savedName+'」に':'OneDriveフォルダに')+'接続してデータを読み込みます。';
      if(quickBtn) quickBtn.style.display='none';
    }
  } else {
    banner.style.display='none';
  }
}

// ── CSV再接続 → データ読み込み → ログイン画面更新 ──
async function reconnectCsvAndLogin(){
  if(!('showDirectoryPicker' in window)){
    alert('このブラウザはFile System Access APIに対応していません。\nChrome または Edge をご使用ください。');
    return;
  }
  try{
    const handle=await window.showDirectoryPicker({mode:'readwrite'});
    csvDirHandle=handle;
    await saveHandleToIDB(handle); // IDBに保存
    const ok=await loadFromCsvDir();
    if(ok){
      syncTasks();
      saveStorageMeta();
      updateStorageIndicator();
      isEditMode=false;
      updateEditModeUI();
      if(currentUserId&&users.find(u=>u.id===currentUserId)){
        hideLoginScreen();
        updateUserUI();
        updateProjectUI();
        renderAll();
      } else {
        renderLoginScreen();
        updateLoginCsvBanner();
      }
    } else {
      const confirmed=confirm('フォルダにデータが見つかりませんでした。\n現在のデータをこのフォルダに書き出しますか？');
      if(confirmed){
        saveStorageMeta();
        saveToLS();
        updateStorageIndicator();
        alert('✅ データを書き出しました。ユーザーを選択してください。');
        renderLoginScreen();
      }
    }
  }catch(e){
    if(e.name!=='AbortError') alert('フォルダの選択に失敗しました: '+e.message);
  }
}

// ── ストレージ設定モーダル ──
function openStorageModal(){
  _selectedStorageOption = storageMode;
  renderStorageModal();
  document.getElementById('storage-modal').classList.add('open');
  if(storageMode === 'csvFile' && csvDirHandle){
    checkLockFile().then(lock=>{
      const info = document.getElementById('storage-lock-info');
      if(lock && info){
        info.style.display = 'block';
        info.innerHTML = `⚠ <b>${lock.lockedBy}</b> が編集中です（${new Date(lock.lockedAt).toLocaleString('ja-JP')}〜）`;
      }
    });
  }
}
function closeStorageModal(){ document.getElementById('storage-modal').classList.remove('open'); }

function renderStorageModal(){
  document.getElementById('storage-opt-ls').className=
    'storage-option'+(_selectedStorageOption==='localStorage'?' selected':'');
  document.getElementById('storage-opt-csv').className=
    'storage-option'+(_selectedStorageOption==='csvFile'?' selected':'');
  document.getElementById('storage-csv-detail').style.display=
    _selectedStorageOption==='csvFile'?'block':'none';
  const info=document.getElementById('storage-csv-folder-info');
  if(csvDirHandle){
    info.innerHTML='✅ <b>'+csvDirHandle.name+'</b> が選択されています';
    info.style.color='var(--success)';
  } else {
    const savedName=getSavedCsvDirName();
    if(savedName){ info.innerHTML='☁️ 前回のフォルダ: <b>'+savedName+'</b>（再選択してください）'; info.style.color='var(--warn)'; }
    else { info.textContent='OneDriveフォルダが選択されていません'; info.style.color='var(--text3)'; }
  }
  const lockInfo=document.getElementById('storage-lock-info');
  if(lockInfo) lockInfo.style.display='none';
}
function selectStorageOption(mode){
  _selectedStorageOption = mode;
  renderStorageModal();
}

// ════════════════════════════════════════════════════
// IndexedDB：FileSystemDirectoryHandle の永続化
// ════════════════════════════════════════════════════
const IDB_NAME='wbs_manager_idb';
const IDB_STORE='handles';
const IDB_KEY='onedrive-folder';

function openIDB(){
  return new Promise((resolve,reject)=>{
    const req=indexedDB.open(IDB_NAME,1);
    req.onupgradeneeded=e=>{
      e.target.result.createObjectStore(IDB_STORE);
    };
    req.onsuccess=e=>resolve(e.target.result);
    req.onerror=e=>reject(e.target.error);
  });
}

async function saveHandleToIDB(handle){
  try{
    const db=await openIDB();
    const tx=db.transaction(IDB_STORE,'readwrite');
    tx.objectStore(IDB_STORE).put(handle,IDB_KEY);
    await new Promise((res,rej)=>{tx.oncomplete=res;tx.onerror=rej;});
  }catch(e){console.warn('IDB save failed:',e);}
}

async function loadHandleFromIDB(){
  try{
    const db=await openIDB();
    return await new Promise((resolve,reject)=>{
      const tx=db.transaction(IDB_STORE,'readonly');
      const req=tx.objectStore(IDB_STORE).get(IDB_KEY);
      req.onsuccess=e=>resolve(e.target.result||null);
      req.onerror=e=>reject(e.target.error);
    });
  }catch(e){console.warn('IDB load failed:',e);return null;}
}

async function clearHandleFromIDB(){
  try{
    const db=await openIDB();
    const tx=db.transaction(IDB_STORE,'readwrite');
    tx.objectStore(IDB_STORE).delete(IDB_KEY);
  }catch(e){}
}

// ── ハンドルの許可を確認・要求 ──
async function verifyHandlePermission(handle){
  try{
    // 既に許可があるか確認
    const perm=await handle.queryPermission({mode:'readwrite'});
    if(perm==='granted') return true;
    // 許可を要求（ユーザーのジェスチャーが必要）
    const req=await handle.requestPermission({mode:'readwrite'});
    return req==='granted';
  }catch(e){return false;}
}

// ── 起動時のIDB復元 ──
async function tryRestoreHandleFromIDB(){
  if(storageMode!=='csvFile') return false;
  const handle=await loadHandleFromIDB();
  if(!handle) return false;
  // 保存済みハンドルを変数にセット（許可確認はまだしない）
  csvDirHandle=handle;
  return true;
}

// ── ワンクリック再接続（許可ダイアログのみ） ──
async function quickReconnect(){
  if(!csvDirHandle){
    // IDBにハンドルがない場合はフォルダ選択
    await reconnectCsvAndLogin();
    return;
  }
  try{
    const granted=await verifyHandlePermission(csvDirHandle);
    if(!granted){
      showToastNotice('⚠ フォルダへのアクセスが拒否されました。再度フォルダを選択してください。','warn');
      csvDirHandle=null;
      await clearHandleFromIDB();
      renderLoginScreen();
      updateLoginCsvBanner();
      return;
    }
    // 許可OK → データ読み込み
    const ok=await loadFromCsvDir();
    if(ok){
      syncTasks();
      saveStorageMeta();
      updateStorageIndicator();
      isEditMode=false;
      updateEditModeUI();
      if(currentUserId&&users.find(u=>u.id===currentUserId)){
        hideLoginScreen();
        updateUserUI();
        updateProjectUI();
        renderAll();
        showToastNotice('☁️ OneDriveに再接続しました','success');
      } else {
        renderLoginScreen();
        updateLoginCsvBanner();
      }
    } else {
      // データなし → 現在のデータを書き出す
      const confirmed=confirm('フォルダにデータが見つかりませんでした。\n現在のデータをこのフォルダに書き出しますか？');
      if(confirmed){
        saveStorageMeta();
        saveToLS();
        updateStorageIndicator();
        showToastNotice('✅ データを書き出しました','success');
        renderLoginScreen();
      }
    }
  }catch(e){
    if(e.name!=='AbortError'){
      showToastNotice('⚠ 再接続に失敗しました: '+e.message,'warn');
    }
  }
}

// ── フォルダ選択時にIDBにも保存 ──
async function selectCsvFolder(){
  if(!('showDirectoryPicker' in window)){
    alert('このブラウザはFile System Access APIに対応していません。\nChrome または Edge をご使用ください。');
    return;
  }
  try{
    const handle=await window.showDirectoryPicker({mode:'readwrite'});
    csvDirHandle=handle;
    await saveHandleToIDB(handle); // IDBに保存
    saveStorageMeta();
    renderStorageModal();
  }catch(e){
    if(e.name!=='AbortError') alert('フォルダの選択に失敗しました: '+e.message);
  }
}

async function applyStorageMode(){
  const newMode=_selectedStorageOption;
  if(newMode==='csvFile'&&!csvDirHandle){ alert('OneDriveフォルダを選択してください。'); return; }
  storageMode=newMode;
  saveStorageMeta();
  saveToLS();
  if(newMode==='csvFile'){
    try{
      const fh=await csvDirHandle.getFileHandle('wbs_data.json');
      const file=await fh.getFile();
      const text=await file.text();
      const existing=JSON.parse(text);
      if(existing.projects&&existing.projects.length){
        const choice=confirm('フォルダに既存データが見つかりました。\n\n[OK] 既存データを読み込む\n[キャンセル] 現在のデータをフォルダに書き込む');
        if(choice){ await loadFromCsvDir(); syncTasks(); updateProjectUI(); renderAll(); }
      }
    }catch(e){}
  }
  isEditMode=storageMode==='localStorage';
  updateStorageIndicator();
  updateEditModeUI();
  closeStorageModal();
}

document.getElementById('storage-modal').addEventListener('click', function(e){
  if(e.target===this) closeStorageModal();
});

// ── 定期ポーリング（CSVモード・30秒ごと） ──
let _pollInterval=null;
function startCsvPolling(){
  if(_pollInterval) clearInterval(_pollInterval);
  _pollInterval=setInterval(async()=>{
    if(storageMode!=='csvFile'||!csvDirHandle) return;

    // ① ロック状態確認→バナー更新
    try{
      const lh=await csvDirHandle.getFileHandle('wbs_lock.json');
      const file=await lh.getFile();
      const lock=JSON.parse(await file.text());
      const banner=document.getElementById('readonly-banner');
      const bannerIcon=document.getElementById('readonly-banner-icon');
      const bannerText=document.getElementById('readonly-banner-text');
      if(lock.locked&&lock.userId!==currentUserId&&new Date(lock.expires)>new Date()){
        if(banner){
          banner.classList.add('visible');
          banner.style.cssText='display:flex;background:#FEF2F2;border-color:#FCA5A5;color:#991B1B';
          if(bannerIcon) bannerIcon.textContent='🔒';
          if(bannerText) bannerText.textContent=lock.lockedBy+' が編集中（'+new Date(lock.lockedAt).toLocaleTimeString('ja-JP')+'〜）';
        }
      } else if(!isEditMode&&banner){
        banner.classList.add('visible');
        banner.style.cssText='';
        if(bannerIcon) bannerIcon.textContent='👁';
        if(bannerText) bannerText.textContent='参照モード';
      }
    }catch(e){}

    // ② データ更新確認
    try{
      const fh=await csvDirHandle.getFileHandle('wbs_data.json');
      const file=await fh.getFile();
      const d=JSON.parse(await file.text());
      const remoteTime=d._savedAt||0;
      const localTime=JSON.parse(localStorage.getItem(LS_KEY)||'{}')._savedAt||0;
      if(remoteTime>localTime+2000){
        if(!isEditMode){
          applyLoadedData(d);
          try{ localStorage.setItem(LS_KEY,JSON.stringify(d)); }catch(e){}
          syncTasks(); updateProjectUI(); renderAll();
          showToastNotice('🔄 データが更新されました（自動リロード）','info');
        } else {
          showToastNotice('⚠ 他のユーザーがデータを更新しました。編集完了後に差異が生じる可能性があります。','warn');
        }
      }
    }catch(e){}
  },30000);
}

function resetToSampleData(){
  if(!confirm('すべてのプロジェクトデータを削除してサンプルデータに戻しますか？\nこの操作は取り消せません。'))return;
  try{ localStorage.removeItem(LS_KEY); }catch(e){}
  const pid=projUid();
  projects=[{id:pid,name:'サンプルプロジェクト',desc:'WBS Managerのサンプルデータです',color:'#2563EB',uidCounter:200,tasks:SAMPLE_TASKS()}];
  currentProjectId=pid;
  syncTasks();
  saveToLS();
  closeStorageModal();
  updateProjectUI();
  renderAll();
  alert('✅ サンプルデータでリセットしました');
}


// ════════════════════════════════════════════════════
let isEditMode=false; // CSVモードでの編集フラグ

// ── 参照/編集モードUI更新 ──
function updateEditModeUI(){
  const isCsv=(storageMode==='csvFile'&&csvDirHandle);
  const banner=document.getElementById('readonly-banner');
  const checkinBtn=document.getElementById('checkin-btn');
  const checkoutBtn=document.getElementById('checkout-btn');
  if(!isCsv){
    banner.classList.remove('visible');
    if(checkinBtn) checkinBtn.style.display='none';
    if(checkoutBtn) checkoutBtn.style.display='none';
    document.body.classList.remove('readonly-mode');
    isEditMode=true;
    return;
  }
  if(isEditMode){
    banner.classList.remove('visible');
    if(checkinBtn) checkinBtn.style.display='none';
    if(checkoutBtn) checkoutBtn.style.display='inline-flex';
    document.body.classList.remove('readonly-mode');
  } else {
    banner.classList.add('visible');
    if(checkinBtn) checkinBtn.style.display='inline-flex';
    if(checkoutBtn) checkoutBtn.style.display='none';
    document.body.classList.add('readonly-mode');
  }
}

async function checkin(){
  if(storageMode!=='csvFile'||!csvDirHandle) return;
  const lock=await checkLockFile();
  if(lock){
    const proceed=confirm('⚠ 現在 '+lock.lockedBy+' が編集中です\n（'+new Date(lock.lockedAt).toLocaleString('ja-JP')+'〜）\n\n強制的に編集を開始しますか？（推奨しません）');
    if(!proceed) return;
  }
  const ok=await loadFromCsvDir();
  if(ok){ syncTasks(); updateProjectUI(); renderAll(); }
  await writeLockFile(true);
  isEditMode=true;
  updateEditModeUI();
  showToastNotice('✏️ 編集モードを開始しました。完了後は「編集完了」を押してください。','success');
}

async function checkout(){
  if(storageMode!=='csvFile'||!csvDirHandle) return;
  saveToLS();
  await writeLockFile(false);
  isEditMode=false;
  updateEditModeUI();
  showToastNotice('✅ 編集完了・チェックアウトしました。','info');
}

// ── ロックファイルの書き込み ──
async function writeLockFile(locked){
  if(!csvDirHandle) return;
  try{
    const cu=currentUser();
    const lock=locked
      ? {
          locked:true,
          lockedBy:cu?cu.name:'Unknown',
          userId:currentUserId,
          lockedAt:new Date().toISOString(),
          expires:new Date(Date.now()+7200000).toISOString() // 2時間
        }
      : {locked:false, lockedBy:null, userId:null, lockedAt:null, expires:null};
    const lh=await csvDirHandle.getFileHandle('wbs_lock.json',{create:true});
    const lw=await lh.createWritable();
    await lw.write(JSON.stringify(lock,null,2));
    await lw.close();
  }catch(e){ console.warn('lock write failed',e); }
}

// ── トースト通知 ──
function showToastNotice(msg, type='info'){
  const existing=document.getElementById('storage-notice');
  if(existing) existing.remove();
  const el=document.createElement('div');
  el.id='storage-notice';
  const bg=type==='success'?'#059669':type==='warn'?'#D97706':'#2563EB';
  el.style.cssText='position:fixed;bottom:24px;left:50%;transform:translateX(-50%);background:'+bg+';color:#fff;padding:10px 20px;border-radius:8px;font-size:12px;z-index:9999;box-shadow:0 4px 12px rgba(0,0,0,.2);max-width:480px;text-align:center;cursor:pointer;transition:.3s';
  el.textContent=msg;
  el.onclick=()=>el.remove();
  document.body.appendChild(el);
  setTimeout(()=>{if(el.parentNode){el.style.opacity='0';setTimeout(()=>el.remove(),300);}},6000);
}

// ── 参照モードでの操作ブロック（保存をスキップ） ──
function saveToLS(){
  if(storageMode==='csvFile'&&csvDirHandle&&!isEditMode){
    // 参照モードでは保存しない（localStorageのみ書く）
    try{
      const data={projects,currentProjectId,_projUid,_uid,users,currentUserId,_savedAt:Date.now()};
      localStorage.setItem(LS_KEY,JSON.stringify(data));
    }catch(e){}
    return;
  }
  const data={projects,currentProjectId,_projUid,_uid,users,currentUserId,_savedAt:Date.now()};
  try{ localStorage.setItem(LS_KEY,JSON.stringify(data)); }catch(e){}
  if(storageMode==='csvFile'&&csvDirHandle&&isEditMode){
    saveToCsvDir(data);
  }
}

// ════════════════════════════════════════════════════
// USER MODEL
//  id, name, role, note, color, createdAt
// ════════════════════════════════════════════════════
const USER_COLORS=['#2563EB','#7C3AED','#059669','#D97706','#DC2626','#0891B2','#65A30D','#DB2777','#374151','#9333EA'];
let users=[];
let currentUserId=null;
let _userUid=1; const userUid=()=>'u'+(_userUid++);

function currentUser(){return users.find(u=>u.id===currentUserId)||null;}
function initials(name){return(name||'?').split(/\s+/).map(w=>w[0]||'').join('').slice(0,2).toUpperCase()||'?';}

// ── Default users ──
const DEFAULT_USERS=()=>[
  {id:userUid(),name:'田中 太郎',role:'プロジェクトマネージャー',note:'',color:'#2563EB',createdAt:new Date().toISOString()},
  {id:userUid(),name:'佐藤 花子',role:'バックエンドエンジニア',note:'',color:'#059669',createdAt:new Date().toISOString()},
  {id:userUid(),name:'鈴木 一郎',role:'フロントエンドエンジニア',note:'',color:'#7C3AED',createdAt:new Date().toISOString()},
  {id:userUid(),name:'山田 美咲',role:'UIデザイナー',note:'',color:'#D97706',createdAt:new Date().toISOString()},
];

// ── Login screen ──
function showLoginScreen(){
  renderLoginScreen();
  document.getElementById('login-screen').style.display='flex';
}
function hideLoginScreen(){
  document.getElementById('login-screen').style.display='none';
}
function renderLoginScreen(){
  const grid=document.getElementById('login-user-grid');
  grid.innerHTML=users.map(u=>`
    <div class="login-user-card" onclick="loginAs('${u.id}')">
      <div class="l-avatar" style="background:${u.color}">${initials(u.name)}</div>
      <div class="l-name">${u.name}</div>
      <div class="l-role">${u.role||'─'}</div>
    </div>`).join('');
}
function loginAs(uid){
  currentUserId=uid;
  hideLoginScreen();
  closeUserPanel();
  saveToLS();
  updateUserUI();
  // pre-fill assignee field with current user
  const inp=document.getElementById('m-assignee');
  if(inp&&!inp.value){const u=currentUser();if(u)inp.value=u.name;}
}

// ── Header user UI ──
function updateUserUI(){
  const u=currentUser();
  document.getElementById('header-user-avatar').style.background=u?u.color:'#9B9890';
  document.getElementById('header-user-avatar').textContent=u?initials(u.name):'?';
  document.getElementById('header-user-name').textContent=u?u.name:'ゲスト';
  renderUserList();
}

// ── User panel (dropdown) ──
function toggleUserPanel(){
  const p=document.getElementById('user-panel');
  p.classList.toggle('open');
  if(p.classList.contains('open'))renderUserList();
}
function closeUserPanel(){document.getElementById('user-panel').classList.remove('open');}
function renderUserList(){
  document.getElementById('user-list').innerHTML=users.map(u=>`
    <div class="user-item${u.id===currentUserId?' active':''}" onclick="loginAs('${u.id}')">
      <div class="uavatar" style="background:${u.color}">
        ${initials(u.name)}
        ${u.id===currentUserId?'<div class="online-dot"></div>':''}
      </div>
      <div class="user-item-info">
        <div class="user-item-name">${u.name}</div>
        <div class="user-item-meta">${u.role||'─'}</div>
      </div>
      <div class="user-item-actions">
        <button class="icon-btn" title="編集" onclick="openEditUserModal('${u.id}',event)" style="font-size:12px;width:24px;height:24px">✏️</button>
        ${users.length>1?`<button class="icon-btn" title="削除" onclick="deleteUser('${u.id}',event)" style="font-size:12px;width:24px;height:24px;color:var(--danger)">🗑</button>`:''}
      </div>
    </div>`).join('');
}

// close panel when clicking outside
document.addEventListener('click',e=>{
  const panel=document.getElementById('user-panel');
  const btn=document.getElementById('user-btn');
  if(panel&&btn&&!panel.contains(e.target)&&!btn.contains(e.target))closeUserPanel();
});

// ── User management modal ──
function openUserMgmtModal(){
  closeUserPanel();
  renderUserMgmtList();
  document.getElementById('user-mgmt-modal').classList.add('open');
}
function closeUserMgmtModal(){document.getElementById('user-mgmt-modal').classList.remove('open');}
function renderUserMgmtList(){
  document.getElementById('user-mgmt-list').innerHTML=users.map(u=>`
    <div style="display:flex;align-items:center;gap:12px;padding:12px 14px;background:var(--surface2);border-radius:var(--radius);border:1px solid var(--border)${u.id===currentUserId?';border-color:var(--accent)':''}">
      <div style="width:40px;height:40px;border-radius:50%;background:${u.color};display:flex;align-items:center;justify-content:center;font-size:14px;font-weight:700;color:#fff;flex-shrink:0">${initials(u.name)}</div>
      <div style="flex:1;min-width:0">
        <div style="font-size:13px;font-weight:600;display:flex;align-items:center;gap:6px">
          ${u.name}
          ${u.id===currentUserId?'<span style="font-size:10px;background:var(--accent);color:#fff;padding:1px 6px;border-radius:10px;font-weight:500">ログイン中</span>':''}
        </div>
        <div style="font-size:11px;color:var(--text3);margin-top:2px">${u.role||'─'}</div>
        ${u.note?`<div style="font-size:11px;color:var(--text2);margin-top:3px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis">${u.note}</div>`:''}
      </div>
      <div style="display:flex;gap:6px;flex-shrink:0">
        <button class="btn btn-sm" onclick="openEditUserModal('${u.id}',event)">✏️ 編集</button>
        ${users.length>1?`<button class="btn btn-sm" style="color:var(--danger)" onclick="deleteUser('${u.id}',event)">🗑</button>`:''}
      </div>
    </div>`).join('');
}

// ── Add / Edit user modal ──
let _editingUserId=null;
let _loginAfterAdd=false;
let _selectedUeColor=USER_COLORS[0];

function openAddUserModal(loginAfterAdd=false){
  _editingUserId=null;
  _loginAfterAdd=loginAfterAdd;
  _selectedUeColor=USER_COLORS[users.length%USER_COLORS.length];
  document.getElementById('user-edit-title').textContent='ユーザーを追加';
  document.getElementById('ue-id').value='';
  document.getElementById('ue-name').value='';
  document.getElementById('ue-role').value='';
  document.getElementById('ue-note').value='';
  renderUeColorPicker();
  document.getElementById('user-edit-modal').classList.add('open');
  setTimeout(()=>document.getElementById('ue-name').focus(),100);
}
function openEditUserModal(uid,e){
  if(e)e.stopPropagation();
  const u=users.find(x=>x.id===uid);if(!u)return;
  _editingUserId=uid;
  _loginAfterAdd=false;
  _selectedUeColor=u.color;
  document.getElementById('user-edit-title').textContent='ユーザーを編集';
  document.getElementById('ue-id').value=uid;
  document.getElementById('ue-name').value=u.name;
  document.getElementById('ue-role').value=u.role||'';
  document.getElementById('ue-note').value=u.note||'';
  renderUeColorPicker();
  // close other modals if open
  document.getElementById('user-mgmt-modal').classList.remove('open');
  document.getElementById('user-panel').classList.remove('open');
  document.getElementById('user-edit-modal').classList.add('open');
  setTimeout(()=>document.getElementById('ue-name').focus(),100);
}
function closeUserEditModal(){
  document.getElementById('user-edit-modal').classList.remove('open');
  _loginAfterAdd=false;
}
function renderUeColorPicker(){
  document.getElementById('ue-color-picker').innerHTML=USER_COLORS.map(c=>`
    <div class="color-swatch${c===_selectedUeColor?' selected':''}" style="background:${c}" onclick="selectUeColor('${c}')" title="${c}"></div>`).join('');
}
function selectUeColor(c){
  _selectedUeColor=c;
  renderUeColorPicker();
}
function submitUserEdit(){
  const name=document.getElementById('ue-name').value.trim();
  if(!name){alert('氏名を入力してください');return;}
  const role=document.getElementById('ue-role').value.trim();
  const note=document.getElementById('ue-note').value.trim();
  if(_editingUserId){
    const u=users.find(x=>x.id===_editingUserId);
    if(u){u.name=name;u.role=role;u.note=note;u.color=_selectedUeColor;}
  }else{
    const newUser={id:userUid(),name,role,note,color:_selectedUeColor,createdAt:new Date().toISOString()};
    users.push(newUser);
    if(_loginAfterAdd){
      closeUserEditModal();
      loginAs(newUser.id);
      saveToLS();
      updateUserUI();
      return;
    }
  }
  closeUserEditModal();
  saveToLS();
  updateUserUI();
  renderUserMgmtList();
  updateAssigneeOptions();
}

// ── Delete user ──
function deleteUser(uid,e){
  if(e)e.stopPropagation();
  const u=users.find(x=>x.id===uid);if(!u)return;
  if(!confirm(`「${u.name}」を削除しますか？\n担当タスクの担当者名はそのまま残ります。`))return;
  users=users.filter(x=>x.id!==uid);
  if(currentUserId===uid){
    currentUserId=users[0]?.id||null;
    if(!currentUserId){showLoginScreen();}
  }
  saveToLS();
  updateUserUI();
  renderUserMgmtList();
}

// ── Assignee select options (inject into modals) ──
function updateAssigneeOptions(){
  const userOptions='<option value="">（未割当）</option>'
    +users.map(u=>'<option value="'+u.name+'">'+u.name+(u.role?' ('+u.role+')':'')+'</option>').join('');
  const datalistHtml=users.map(u=>'<option value="'+u.name+'">').join('');

  // セレクトを更新
  ['m-assignee-select','dp-assignee-select'].forEach(id=>{
    const sel=document.getElementById(id);
    if(!sel)return;
    const cur=sel.value;
    sel.innerHTML=userOptions;
    sel.value=cur; // 現在値を維持
  });
  // datalistを更新
  ['m-assignee-list','dp-assignee-list'].forEach(id=>{
    const dl=document.getElementById(id);
    if(dl) dl.innerHTML=datalistHtml;
  });
}

// セレクトで選択 → テキスト入力に反映
function onAssigneeSelectChange(prefix){
  const sel=document.getElementById(prefix+'-assignee-select');
  const inp=document.getElementById(prefix+'-assignee');
  if(!sel||!inp)return;
  inp.value=sel.value;
  if(prefix==='dp') dpUpdate('assignee',sel.value);
}
// テキスト入力で変更 → セレクトに反映（一致するユーザーがあれば選択）
function onAssigneeInputChange(prefix){
  const inp=document.getElementById(prefix+'-assignee');
  const sel=document.getElementById(prefix+'-assignee-select');
  if(!inp||!sel)return;
  const matched=users.find(u=>u.name===inp.value.trim());
  sel.value=matched?matched.name:'';
}
// 担当者フィールドを値でセット（セレクト・入力欄両方同期）
function setAssigneeField(prefix, value){
  const inp=document.getElementById(prefix+'-assignee');
  const sel=document.getElementById(prefix+'-assignee-select');
  if(inp) inp.value=value||'';
  if(sel){
    const matched=users.find(u=>u.name===value);
    sel.value=matched?matched.name:'';
  }
}

// ── Init users ──
function initUsers(){
  if(!users.length){
    // 初回起動：デフォルトユーザーを生成して先頭を自動ログイン
    users=DEFAULT_USERS();
    currentUserId=users[0].id;
    saveToLS();
    hideLoginScreen();
    updateUserUI();
    updateAssigneeOptions();
    return;
  }
  // 保存済みユーザーがある場合
  if(!currentUserId || !users.find(u=>u.id===currentUserId)){
    // currentUserIdが無効 → ログイン画面表示
    updateLoginCsvBanner();
    showLoginScreen();
  } else {
    hideLoginScreen();
  }
  updateUserUI();
  updateAssigneeOptions();
}

// ── backdrop close for user modals ──
['user-edit-modal','user-mgmt-modal'].forEach(id=>{
  document.getElementById(id).addEventListener('click',function(e){if(e.target===this)this.classList.remove('open');});
});

// ── Project list ──
let projects=[];
let currentProjectId=null;

function currentProject(){return projects.find(p=>p.id===currentProjectId)||projects[0];}

// tasks is always a live reference to currentProject().tasks
let tasks=[];
function syncTasks(){tasks=currentProject()?.tasks||[];}

let _uid=100;
const uid=()=>'t'+(_uid++);

// ─── Init projects ───
// 旧データ（2025年サンプル）を2026年に自動マイグレーション
function migrateSampleDates(){
  const MIGRATE_KEY='wbs_date_migrated_2026';
  if(localStorage.getItem(MIGRATE_KEY)) return; // 実行済み
  const cutoff='2025-08-01'; // この日付より前のデータは移行対象
  let migrated=false;
  projects.forEach(proj=>{
    proj.tasks.forEach(t=>{
      if(t.start&&t.start<cutoff){
        // 2025年 → 2026年にシフト（+365日 or +366日）
        const shift=d=>{
          if(!d)return d;
          const dt=new Date(d);
          dt.setFullYear(dt.getFullYear()+1);
          return dt.toISOString().slice(0,10);
        };
        t.start=shift(t.start);
        t.end=shift(t.end);
        migrated=true;
      }
    });
  });
  if(migrated){
    saveToLS();
    localStorage.setItem(MIGRATE_KEY,'1');
    console.log('WBS Manager: sample dates migrated to 2026');
  }else{
    localStorage.setItem(MIGRATE_KEY,'1');
  }
}

function initProjects(){
  if(loadFromLS()){
    syncTasks();
    migrateSampleDates(); // ← 旧データを自動マイグレーション
    syncTasks();
    return;
  }
  // Default: one sample project
  const pid=projUid();
  projects=[{
    id:pid, name:'サンプルプロジェクト', desc:'WBS Managerのサンプルデータです',
    color:'#2563EB', uidCounter:200,
    tasks:SAMPLE_TASKS()
  }];
  currentProjectId=pid;
  syncTasks();
  saveToLS();
}

// ── Switch project ──
function switchProject(pid){
  saveCurrentTasks(); // save before switching
  currentProjectId=pid;
  syncTasks();
  collapsedSet.clear();
  selectedTaskId=null;
  document.getElementById('detail-panel').classList.remove('open');
  updateProjectUI();
  renderAll();
  saveToLS();
}
function saveCurrentTasks(){
  const p=currentProject();
  if(p)p.tasks=[...tasks];
}

// ── Update all project UI elements ──
function updateProjectUI(){
  const p=currentProject();
  if(!p)return;

  // header select
  const sel=document.getElementById('header-proj-select');
  sel.innerHTML=projects.map(pr=>`<option value="${pr.id}"${pr.id===currentProjectId?' selected':''}>${pr.name}</option>`).join('');
  document.getElementById('header-proj-dot').style.background=p.color;

  // sidebar list
  const list=document.getElementById('sidebar-proj-list');
  list.innerHTML=projects.map(pr=>{
    const taskCount=pr.tasks.length;
    const doneCount=pr.tasks.filter(t=>t.status==='done').length;
    const isActive=pr.id===currentProjectId;
    return `<div class="proj-list-item${isActive?' active':''}" onclick="switchProject('${pr.id}')" id="projitem-${pr.id}">
      <div class="proj-dot" style="background:${pr.color}"></div>
      <span class="proj-name" id="projname-${pr.id}">${pr.name}</span>
      <span class="proj-count">${doneCount}/${taskCount}</span>
      <div class="proj-actions">
        <button class="icon-btn" title="名前を編集" onclick="startRenameProject('${pr.id}',event)" style="font-size:12px;width:22px;height:22px">✏️</button>
        ${projects.length>1?`<button class="icon-btn" title="削除" onclick="deleteProject('${pr.id}',event)" style="font-size:12px;width:22px;height:22px;color:var(--danger)">🗑</button>`:''}
      </div>
    </div>`;
  }).join('');

  // page title
  document.title=`${p.name} — WBS Manager`;
}

// ── Rename project inline ──
function startRenameProject(pid,e){
  e.stopPropagation();
  const nameEl=document.getElementById(`projname-${pid}`);
  if(!nameEl)return;
  const p=projects.find(x=>x.id===pid);
  nameEl.outerHTML=`<input class="proj-edit-input" id="projinput-${pid}" value="${p.name}"
    onblur="finishRenameProject('${pid}')"
    onkeydown="if(event.key==='Enter')finishRenameProject('${pid}');if(event.key==='Escape')updateProjectUI()">`;
  setTimeout(()=>{const el=document.getElementById(`projinput-${pid}`);if(el){el.focus();el.select();}},50);
}
function finishRenameProject(pid){
  const el=document.getElementById(`projinput-${pid}`);
  if(!el)return;
  const name=el.value.trim();
  const p=projects.find(x=>x.id===pid);
  if(p&&name)p.name=name;
  saveToLS();
  updateProjectUI();
}

// ── Delete project ──
function deleteProject(pid,e){
  e.stopPropagation();
  const p=projects.find(x=>x.id===pid);
  if(!p)return;
  if(!confirm(`「${p.name}」を削除しますか？\nこのプロジェクトのすべてのタスクが削除されます。`))return;
  projects=projects.filter(x=>x.id!==pid);
  if(currentProjectId===pid)currentProjectId=projects[0].id;
  syncTasks();
  saveToLS();
  updateProjectUI();
  renderAll();
}

// ── New project modal ──
let selectedNewProjColor=PROJ_COLORS[0];
function openNewProjectModal(){
  document.getElementById('np-name').value='';
  document.getElementById('np-desc').value='';
  document.getElementById('np-template').value='blank';
  selectedNewProjColor=PROJ_COLORS[projects.length%PROJ_COLORS.length];
  // render color picker
  document.getElementById('np-color-picker').innerHTML=PROJ_COLORS.map(c=>`
    <div onclick="selectNewProjColor('${c}')" id="npcolor-${c.replace('#','')}"
      style="width:24px;height:24px;border-radius:50%;background:${c};cursor:pointer;border:3px solid ${c===selectedNewProjColor?'#1A1917':'transparent'};transition:.12s"
      title="${c}"></div>`).join('');
  document.getElementById('new-proj-modal').classList.add('open');
  setTimeout(()=>document.getElementById('np-name').focus(),100);
}
function selectNewProjColor(c){
  selectedNewProjColor=c;
  document.querySelectorAll('#np-color-picker > div').forEach(el=>{
    const elColor='#'+el.id.replace('npcolor-','');
    el.style.borderColor=elColor===c?'#1A1917':'transparent';
  });
}
function closeNewProjectModal(){document.getElementById('new-proj-modal').classList.remove('open');}
function submitNewProject(){
  const name=document.getElementById('np-name').value.trim();
  if(!name){alert('プロジェクト名を入力してください');return;}
  const desc=document.getElementById('np-desc').value.trim();
  const template=document.getElementById('np-template').value;
  saveCurrentTasks();
  const pid=projUid();
  const newProj={
    id:pid, name, desc, color:selectedNewProjColor,
    tasks: template==='basic' ? SAMPLE_TASKS() : []
  };
  projects.push(newProj);
  currentProjectId=pid;
  syncTasks();
  collapsedSet.clear();
  selectedTaskId=null;
  document.getElementById('detail-panel').classList.remove('open');
  closeNewProjectModal();
  saveToLS();
  updateProjectUI();
  renderAll();
}
document.getElementById('new-proj-modal').addEventListener('click',function(e){if(e.target===this)closeNewProjectModal();});

// ─── Display number: 動的に "1", "1.1", "2.3.1" などを計算 ───
function calcDisplayNums(){
  const nums={};
  function walk(parentId, prefix){
    const children=tasks.filter(t=>t.parentId===parentId);
    children.forEach((t,i)=>{
      const n = prefix ? prefix+'.'+(i+1) : String(i+1);
      nums[t.id]=n;
      walk(t.id, n);
    });
  }
  walk(null,'');
  return nums;
}

const ASSIGNEE_COLORS={};
const COLOR_POOL=['#2563EB','#7C3AED','#059669','#D97706','#DC2626','#0891B2','#65A30D'];
let colorIdx=0;
function getAssigneeColor(name){
  if(!name)return'#9B9890';
  if(!ASSIGNEE_COLORS[name]){ASSIGNEE_COLORS[name]=COLOR_POOL[colorIdx%COLOR_POOL.length];colorIdx++;}
  return ASSIGNEE_COLORS[name];
}

const STATUS_LABEL={todo:'未着手',doing:'進行中',done:'完了',block:'ブロック中'};
const STATUS_CLASS={todo:'s-todo',doing:'s-doing',done:'s-done',block:'s-block'};
const STATUS_DOT  ={todo:'●',doing:'◑',done:'✓',block:'✕'};


// ─── Tree helpers ───
function hasChildren(id){return tasks.some(t=>t.parentId===id);}
function getLevel(id){
  let lvl=0,cur=tasks.find(t=>t.id===id);
  while(cur&&cur.parentId){lvl++;cur=tasks.find(t=>t.id===cur.parentId);}
  return lvl;
}
function isAncestorCollapsed(task){
  let cur=tasks.find(t=>t.id===task.parentId);
  while(cur){if(collapsedSet.has(cur.id))return true;cur=tasks.find(t=>t.id===cur.parentId);}
  return false;
}
function buildTreeOrder(parentId=null,result=[]){
  tasks.filter(t=>t.parentId===parentId).forEach(t=>{
    result.push(t);
    if(!collapsedSet.has(t.id))buildTreeOrder(t.id,result);
  });
  return result;
}

// ─── Render List ───
function renderList(){
  const tbody=document.getElementById('wbs-tbody');
  const nums=calcDisplayNums();
  const treeOrder=buildTreeOrder();
  const conflictMap=buildConflictMap(); // ← 矛盾マップ
  const q=(document.getElementById('search-input')||{value:''}).value.toLowerCase();
  const fs=(document.getElementById('filter-status')||{value:''}).value;
  const fa=(document.getElementById('filter-assignee')||{value:''}).value;
  const today=new Date();today.setHours(0,0,0,0);
  const formatDate=d=>{if(!d)return'-';const dt=new Date(d);return dt.toLocaleDateString('ja-JP',{month:'2-digit',day:'2-digit'});};

  let html='';
  treeOrder.forEach(t=>{
    if(q&&!t.name.toLowerCase().includes(q)&&!(t.deliverable||'').toLowerCase().includes(q))return;
    if(fs&&t.status!==fs)return;
    if(fa&&t.assignee!==fa)return;

    const lvl=getLevel(t.id);
    const hasCh=hasChildren(t.id);
    const isCol=collapsedSet.has(t.id);
    const isSelected=t.id===selectedTaskId;
    const isFolder=t.type==='folder';
    const dispNum=nums[t.id]||'';

    // indent
    let indentHtml='';
    for(let i=0;i<lvl;i++)indentHtml+=`<span class="indent-spacer"></span>`;

    // toggle
    const toggleHtml=hasCh
      ?`<button class="toggle-btn" onclick="toggleCollapse('${t.id}',event)">${isCol?'▶':'▼'}</button>`
      :`<button class="toggle-btn leaf">　</button>`;

    // icon: folder open/closed vs task
    const icon = isFolder
      ? (isCol||!hasCh ? '📁' : '📂')
      : '📄';

    // ── 矛盾チェック ──
    // フォルダ：自分の子孫に矛盾があるか
    const folderConflicts=isFolder?conflictMap.get(t.id)||[]:[];
    const folderHasConflict=folderConflicts.length>0;
    // タスク：自分がどこかのフォルダ矛盾に含まれているか
    const taskConflictReasons=!isFolder?getTaskConflictReasons(t.id,conflictMap):[];
    const taskHasConflict=taskConflictReasons.length>0;

    // row bg tint for folders
    const rowBg=isFolder
      ?(folderHasConflict?'background:rgba(220,38,38,.04)':'background:rgba(37,99,235,.03)')
      :(taskHasConflict?'background:rgba(220,38,38,.03)':'');
    const nameFw=isFolder?'font-weight:600':'';

    // status (フォルダは薄く)
    const statusHtml=`<span class="status-badge ${STATUS_CLASS[t.status]}" style="${isFolder?'opacity:.7':''}">${STATUS_DOT[t.status]} ${STATUS_LABEL[t.status]}</span>`;

    // assignee
    const acolor=getAssigneeColor(t.assignee);
    const initials=t.assignee?t.assignee.split(' ').map(w=>w[0]||'').join('').slice(0,2).toUpperCase():'?';
    const assigneeHtml=t.assignee
      ?`<span class="assignee-chip"><span class="avatar" style="background:${acolor}">${initials}</span>${t.assignee}</span>`
      :`<span style="color:var(--text3);font-size:12px">-</span>`;

    // dates
    let endClass='date-text';
    if(t.end){const ed=new Date(t.end);ed.setHours(0,0,0,0);if(ed<today&&t.status!=='done')endClass='date-text overdue';else if(ed.getTime()===today.getTime())endClass='date-text today';}

    // progress
    const pct=effectiveProgress(t);
    const pcolor=pct===100?'var(--success)':pct>50?'var(--accent)':'var(--warn)';
    const progressHtml=`<div class="progress-wrap"><div class="progress-bar"><div class="progress-fill" style="width:${pct}%;background:${pcolor}"></div></div><span class="progress-text">${pct}%</span></div>`;

    // deps (display numbers)
    const depsHtml=t.deps&&t.deps.length
      ?t.deps.map(d=>`<span class="dep-chip">${nums[d]||d}</span>`).join('')
      :`<span style="color:var(--text3);font-size:11px">-</span>`;

    // type badge
    const typeBadge=isFolder
      ?`<span style="font-size:9px;background:#EEF3FF;color:var(--accent);border:1px solid #BFDBFE;border-radius:3px;padding:1px 5px;font-weight:600;flex-shrink:0">FOLDER</span>`
      :`<span style="font-size:9px;background:var(--surface2);color:var(--text3);border:1px solid var(--border);border-radius:3px;padding:1px 5px;flex-shrink:0">TASK</span>`;

    // 矛盾警告バッジ
    const conflictBadge=folderHasConflict
      ?`<span title="${folderConflicts.length}件の子孫タスクがフォルダ期間を超えています&#10;${folderConflicts.map(c=>{const ct=tasks.find(x=>x.id===c.taskId);return(ct?ct.name:'?')+': '+c.reason;}).join('&#10;')}"
          style="font-size:10px;background:var(--danger-light);color:var(--danger);border:1px solid #FCA5A5;border-radius:3px;padding:1px 6px;font-weight:600;flex-shrink:0;cursor:help">⚠ ${folderConflicts.length}件</span>`
      :taskHasConflict
      ?`<span title="${taskConflictReasons.join('&#10;')}"
          style="font-size:10px;background:var(--danger-light);color:var(--danger);border:1px solid #FCA5A5;border-radius:3px;padding:1px 6px;font-weight:600;flex-shrink:0;cursor:help">⚠</span>`
      :'';

    // 日付セル（矛盾タスクは赤背景）
    const dateCellStyle=taskHasConflict?'background:rgba(220,38,38,.08);border-radius:3px;padding:1px 4px':'';
    const startCellHtml=`<span class="date-text" style="${dateCellStyle}" title="${taskHasConflict?taskConflictReasons.join('\n'):''}">${formatDate(t.start)}</span>`;
    const endCellHtml=`<span class="${endClass}" style="${dateCellStyle}" title="${taskHasConflict?taskConflictReasons.join('\n'):''}">${formatDate(t.end)}</span>`;

    html+=`<tr class="task-row level-${lvl}${isSelected?' selected':''}" data-id="${t.id}" style="${rowBg}"
      onclick="selectTask('${t.id}')"
      oncontextmenu="openCtxMenu(event,'${t.id}')"
      draggable="true"
      ondragstart="onRowDragStart(event,'${t.id}')"
      ondragover="onRowDragOver(event,'${t.id}')"
      ondragleave="onRowDragLeave(event,'${t.id}')"
      ondrop="onRowDrop(event,'${t.id}')"
      ondragend="onRowDragEnd(event)">
      <td class="td-cell" style="padding:4px 8px;width:80px;white-space:nowrap">
        <div class="drag-handle" title="ドラッグして並べ替え" onmousedown="event.stopPropagation()">⠿</div>
        <div class="row-actions" style="opacity:1;gap:1px;display:inline-flex;align-items:center">
          <!-- 同列追加 -->
          <button class="icon-btn add-sibling-btn" title="同じ階層にタスクを追加" onclick="openAddModal('${t.parentId||''}',event)" style="width:26px;height:26px;color:var(--text3)">
            <svg viewBox="0 0 16 16" width="14" height="14" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round">
              <rect x="1" y="2" width="14" height="4" rx="1"/>
              <rect x="1" y="10" width="14" height="4" rx="1" stroke-dasharray="2.5 1.5" opacity=".5"/>
              <line x1="8" y1="7" x2="8" y2="9.2"/>
            </svg>
          </button>
          <!-- 子追加 -->
          <button class="icon-btn add-child-btn" title="子タスクを追加" onclick="openAddModal('${t.id}',event)" style="width:26px;height:26px;color:var(--accent)">
            <svg viewBox="0 0 16 16" width="14" height="14" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round">
              <rect x="1" y="2" width="9" height="4" rx="1"/>
              <path d="M4 6 L4 11 L5.5 11"/>
              <rect x="5" y="9" width="9" height="4" rx="1"/>
              <line x1="12" y1="7.5" x2="12" y2="9"/>
              <line x1="10.5" y1="8.2" x2="13.5" y2="8.2"/>
            </svg>
          </button>
          <!-- 削除 -->
          <button class="icon-btn" title="削除" onclick="deleteTask('${t.id}',event)" style="width:26px;height:26px;color:var(--text3)">
            <svg viewBox="0 0 16 16" width="14" height="14" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round">
              <path d="M2 4h12M6 4V2.5a.5.5 0 01.5-.5h3a.5.5 0 01.5.5V4M5 4l.7 8.5a.5.5 0 00.5.5h3.6a.5.5 0 00.5-.5L11 4"/>
              <line x1="6.5" y1="7" x2="6.8" y2="11"/>
              <line x1="9.5" y1="7" x2="9.2" y2="11"/>
            </svg>
          </button>
        </div>
      </td>
      <td class="td-cell" style="text-align:center;font-family:'DM Mono',monospace;font-size:11px;color:var(--text3);width:60px">${dispNum}</td>
      <td class="td-name" style="padding-left:12px">
        ${indentHtml}${toggleHtml}
        <span class="task-icon">${icon}</span>
        <div class="task-name-inner">
          <span class="task-name-text" style="${nameFw}">${t.name}</span>
          ${t.deliverable?`<span class="task-deliverable">📎 ${t.deliverable}</span>`:''}
        </div>
        ${typeBadge}${conflictBadge}
      </td>
      <td class="td-cell">${statusHtml}</td>
      <td class="td-cell">${assigneeHtml}</td>
      <td class="td-cell">${startCellHtml}</td>
      <td class="td-cell">${endCellHtml}</td>
      <td class="td-cell">${isFolder
        ? `<div class="progress-wrap" title="子タスク加重平均（自動計算）"><div class="progress-bar"><div class="progress-fill" style="width:${pct}%;background:${pcolor}"></div></div><span class="progress-text" style="color:var(--text3)">${pct}%</span></div>`
        : progressHtml}</td>
      <td class="td-cell"><div class="dep-list">${depsHtml}</div></td>
    </tr>`;
  });

  tbody.innerHTML=html||`<tr><td colspan="9"><div class="empty-state"><div class="icon">🗂</div><p>タスクが見つかりません</p></div></td></tr>`;
  updateStats();
  updateAssigneeFilter();
}

// ─── Gantt ───
const DAY_W=28,ROW_H=38,LABEL_W=320,HDR_MONTH=24,HDR_DAY=22;

// ── Gantt state ──
let ganttMinD=null;
let ganttDragState=null;
let ganttDepLinkState=null;
let ganttHoverDepTarget=null;
let showLightningLine=false;
let _ganttFirstRender=true; // Todayを中央表示するのは初回のみ

// ── スケール設定 ──
let ganttScale='day'; // 'day'|'week'|'month'|'quarter'|'year'
const SCALE_COL_W={day:28, week:56, month:112, quarter:224, year:336};

function setGanttScale(scale){
  ganttScale=scale;
  document.querySelectorAll('.gantt-scale-btn').forEach(b=>{
    b.classList.toggle('active',b.dataset.scale===scale);
  });
  const scrollEl=document.getElementById('gantt-root');
  const prevSX=scrollEl?scrollEl.scrollLeft:0;
  renderGantt();
  requestAnimationFrame(()=>{
    const el=document.getElementById('gantt-root');
    if(!el)return;
    // Todayが中央に来るようにスクロール
    const tx=ganttScaleDateToX(new Date());
    el.scrollLeft=Math.max(0,tx-el.clientWidth/2);
  });
}

// スケール別：日付→X座標（チャートエリア内ピクセル）
function ganttScaleDateToX(dt){
  if(!ganttMinD)return 0;
  const d=new Date(typeof dt==='string'?dt:d2s(dt));
  d.setHours(0,0,0,0);
  const cw=SCALE_COL_W[ganttScale];
  if(ganttScale==='day'){
    return Math.round((d-ganttMinD)/86400000)*cw+cw/2;
  }
  if(ganttScale==='week'){
    const base=new Date(ganttMinD);
    const dow=base.getDay(); base.setDate(base.getDate()-(dow===0?6:dow-1));
    const diffD=Math.round((d-base)/86400000);
    return Math.floor(diffD/7)*cw+cw/2;
  }
  if(ganttScale==='month'){
    const mo=(d.getFullYear()-ganttMinD.getFullYear())*12+(d.getMonth()-ganttMinD.getMonth());
    const daysInMo=new Date(d.getFullYear(),d.getMonth()+1,0).getDate();
    return mo*cw+Math.round((d.getDate()-1)/daysInMo*cw)+cw/14;
  }
  if(ganttScale==='quarter'){
    const qMin=ganttMinD.getFullYear()*4+Math.floor(ganttMinD.getMonth()/3);
    const qCur=d.getFullYear()*4+Math.floor(d.getMonth()/3);
    const qOff=qCur-qMin;
    const mInQ=d.getMonth()%3;
    return qOff*cw+Math.round(mInQ/3*cw)+cw/6;
  }
  if(ganttScale==='year'){
    const yOff=d.getFullYear()-ganttMinD.getFullYear();
    const dayOfYear=Math.floor((d-new Date(d.getFullYear(),0,0))/86400000);
    const isLeap=y=>y%4===0&&(y%100!==0||y%400===0);
    const diy=isLeap(d.getFullYear())?366:365;
    return yOff*cw+Math.round(dayOfYear/diy*cw);
  }
  return 0;
}

// スケール別：上位・下位ヘッダー列を生成
function buildScaleColumns(minD,maxD){
  const cw=SCALE_COL_W[ganttScale];
  const upper=[],lower=[];
  const today=new Date();today.setHours(0,0,0,0);

  if(ganttScale==='day'){
    let cur=new Date(minD);
    while(cur<=maxD){
      const key=cur.getFullYear()+'-'+cur.getMonth();
      if(!upper.length||upper[upper.length-1].key!==key)
        upper.push({key,label:cur.getFullYear()+'年'+(cur.getMonth()+1)+'月',count:0});
      upper[upper.length-1].count++;
      const isWk=cur.getDay()===0||cur.getDay()===6;
      const isTdy=cur.getTime()===today.getTime();
      lower.push({label:String(cur.getDate()),isTdy,isWk,date:new Date(cur)});
      cur.setDate(cur.getDate()+1);
    }
  } else if(ganttScale==='week'){
    let wS=new Date(minD);
    const dow=wS.getDay();wS.setDate(wS.getDate()-(dow===0?6:dow-1));
    let cur=new Date(wS);
    while(cur<=maxD){
      const wE=new Date(cur);wE.setDate(wE.getDate()+6);
      const key=cur.getFullYear()+'-'+cur.getMonth();
      if(!upper.length||upper[upper.length-1].key!==key)
        upper.push({key,label:cur.getFullYear()+'年'+(cur.getMonth()+1)+'月',count:0});
      upper[upper.length-1].count++;
      const isTdy=today>=cur&&today<=wE;
      lower.push({label:(cur.getMonth()+1)+'/'+(cur.getDate()),isTdy,isWk:false,date:new Date(cur)});
      cur.setDate(cur.getDate()+7);
    }
  } else if(ganttScale==='month'){
    let cur=new Date(minD.getFullYear(),minD.getMonth(),1);
    while(cur<=maxD){
      const key=String(cur.getFullYear());
      if(!upper.length||upper[upper.length-1].key!==key)
        upper.push({key,label:cur.getFullYear()+'年',count:0});
      upper[upper.length-1].count++;
      const isTdy=cur.getFullYear()===today.getFullYear()&&cur.getMonth()===today.getMonth();
      lower.push({label:(cur.getMonth()+1)+'月',isTdy,isWk:false,date:new Date(cur)});
      cur.setMonth(cur.getMonth()+1);
    }
  } else if(ganttScale==='quarter'){
    let y=minD.getFullYear(),q=Math.floor(minD.getMonth()/3);
    const endY=maxD.getFullYear(),endQ=Math.floor(maxD.getMonth()/3);
    while(y<endY||(y===endY&&q<=endQ)){
      const key=String(y);
      if(!upper.length||upper[upper.length-1].key!==key)
        upper.push({key,label:y+'年',count:0});
      upper[upper.length-1].count++;
      const isTdy=y===today.getFullYear()&&q===Math.floor(today.getMonth()/3);
      lower.push({label:'Q'+(q+1),isTdy,isWk:false,date:new Date(y,q*3,1)});
      q++;if(q>3){q=0;y++;}
    }
  } else if(ganttScale==='year'){
    let y=minD.getFullYear();
    while(y<=maxD.getFullYear()){
      upper.push({key:String(y),label:'',count:1});
      lower.push({label:y+'年',isTdy:y===today.getFullYear(),isWk:false,date:new Date(y,0,1)});
      y++;
    }
  }
  return {upper,lower,cw};
}

// ── Date helpers ──
const d2s = d => { // Date → "YYYY-MM-DD"
  const y=d.getFullYear(),m=String(d.getMonth()+1).padStart(2,'0'),dd=String(d.getDate()).padStart(2,'0');
  return `${y}-${m}-${dd}`;
};
const s2d = s => { const d=new Date(s); d.setHours(0,0,0,0); return d; };
const addDays = (d,n) => { const r=new Date(d); r.setDate(r.getDate()+n); return r; };

function ganttDateRange(){
  const all=tasks.filter(t=>t.start&&t.end);
  if(!all.length){
    const t=new Date(); t.setDate(1);
    return {minD:t, maxD:addDays(t,60)};
  }
  let minD=s2d(all[0].start), maxD=s2d(all[0].end);
  all.forEach(t=>{
    const s=s2d(t.start),e=s2d(t.end);
    if(s<minD)minD=s; if(e>maxD)maxD=e;
  });
  minD=new Date(minD); minD.setDate(1);
  maxD=addDays(maxD,10);
  return {minD,maxD};
}

function pxToDay(px){ return Math.round(px/DAY_W); }
function dayToPx(off){ return off*DAY_W; }
function dateToOff(dt){ const x=s2d(typeof dt==='string'?dt:d2s(dt)); return Math.round((x-ganttMinD)/86400000); }

// ════════════════════════════════════════════════════
// フォルダ進捗自動計算（全子孫タスクの期間加重平均）
// ════════════════════════════════════════════════════
function calcFolderProgress(folderId){
  const desc=getAllDescendants(folderId).filter(t=>t.type==='task'&&t.start&&t.end);
  if(!desc.length) return 0;
  let totalDays=0, doneDays=0;
  desc.forEach(t=>{
    const dur=Math.max(1, Math.round((s2d(t.end)-s2d(t.start))/86400000)+1);
    totalDays+=dur;
    doneDays+=dur*(t.progress||0)/100;
  });
  return totalDays>0 ? Math.round(doneDays/totalDays*100) : 0;
}

// タスク／フォルダに関わらず実効進捗を返す
function effectiveProgress(t){
  if(t.type==='folder') return calcFolderProgress(t.id);
  return t.progress||0;
}

// ════════════════════════════════════════════════════
// イナズマ線
//
// 対象タスク（フォルダ除外・日程必須）：
//   A) 進行中期間タスク : start <= today <= end
//   B) 遅延タスク      : end < today かつ status !== 'done'
//      （期間が過ぎているのに未完了・未着手のタスク）
//
// 除外：
//   - start > today  （将来タスク・まだ始まっていない）
//   - status === 'done' かつ end < today （正常完了済み）
//   - フォルダ・日程なし
//
// 今日ラインを基準として実績進捗点を縦につなぐ
//   実績点 >= 今日ライン → 進んでいる（青）
//   実績点 <  今日ライン → 遅れている（赤）
// ════════════════════════════════════════════════════
function buildLightningLineHTML(treeOrder, totalH){
  const today=new Date(); today.setHours(0,0,0,0);
  const todayX=dateToOff(today)*DAY_W+DAY_W/2;

  const points=[];

  treeOrder.forEach((t,ri)=>{
    if(t.type==='folder') return;
    if(!t.start||!t.end) return;

    const start=s2d(t.start), end=s2d(t.end);

    // 将来タスク（まだ始まっていない）→ 除外
    if(start > today) return;

    // 正常完了済み（期間内に完了）→ 除外
    if(t.status==='done' && end < today) return;

    // ここに来るのは：
    //   start <= today かつ（期間中 OR 期間終了で未完了）
    const isOverdue = end < today; // 期間超過フラグ

    const pct=t.progress||0;
    const barLeft=dateToOff(t.start)*DAY_W;
    const barRight=(dateToOff(t.end)+1)*DAY_W;
    const barWidth=barRight-barLeft;

    // 実績進捗点のX（バー左端 + 実績%）
    const actualX=barLeft+barWidth*(pct/100);

    // 進み・遅れは今日ラインとの比較
    const ahead=actualX >= todayX;

    // 予定進捗率（経過日数 / 総日数、期間超過なら100%が予定）
    const durDays=Math.max(1,Math.round((end-start)/86400000)+1);
    const elapsedDays=Math.round((today-start)/86400000);
    const plannedPct=isOverdue ? 100 : Math.min(100,Math.round(elapsedDays/durDays*100));

    const y=ri*ROW_H+ROW_H/2;
    const statusLabel={todo:'未着手',doing:'進行中',done:'完了',block:'ブロック中'}[t.status]||'';
    const overdueLabel=isOverdue?' ⚠遅延':'';
    points.push({
      x:actualX, y, ahead, isOverdue,
      label:t.name+': 実績'+pct+'% / 予定'+plannedPct+'%（'+statusLabel+overdueLabel+'）'
    });
  });

  if(!points.length) return '';

  // ── 始点・終点の菱形アンカー ──
  // 始点：チャート上端（最初の対象行の1行上）、X = todayX
  const startY = points[0].y - ROW_H;
  // 終点：最後の対象行の1行下
  const endY   = points[points.length-1].y + ROW_H;

  const diamond=(cx,cy,r,color,tip)=>
    '<polygon points="'+cx+','+(cy-r)+' '+(cx+r)+','+cy+' '+cx+','+(cy+r)+' '+(cx-r)+','+cy+'"'
    +' fill="'+color+'" stroke="#fff" stroke-width="2" opacity=".95">'
    +(tip?'<title>'+tip+'</title>':'')
    +'</polygon>';

  const startDiamond=diamond(todayX, startY, 7, 'var(--accent)', '始点: TODAY');
  const endDiamond  =diamond(todayX, endY,   7, 'var(--accent)', '終点: TODAY');

  // ── 今日ライン基準の縦補助線（始点〜終点を貫通） ──
  const baselineSvg=
    '<line x1="'+todayX+'" y1="'+startY+'" x2="'+todayX+'" y2="'+endY+'"'
    +' stroke="var(--accent)" stroke-width="1" stroke-dasharray="3,3" opacity=".25"/>';

  // ── 始点 → 全実績点 → 終点 を一本の折れ線でつなぐ ──
  // 全点リスト（始点・各タスク点・終点）
  const allPts=[
    {x:todayX, y:startY, ahead:true, isAnchor:true},
    ...points,
    {x:todayX, y:endY,   ahead:true, isAnchor:true}
  ];

  let segSvg='';
  for(let i=0;i<allPts.length-1;i++){
    const p1=allPts[i], p2=allPts[i+1];
    // アンカー→最初の点、最後の点→アンカーはアクセント色
    let c;
    if(p1.isAnchor||p2.isAnchor){
      c='var(--accent)';
    } else {
      // 区間の両端が今日ラインより左なら赤、両端とも右なら青、混在は橙
      const p1Left=p1.x < todayX, p2Left=p2.x < todayX;
      c = p1Left&&p2Left ? '#DC2626' : (!p1Left&&!p2Left ? '#2563EB' : '#D97706');
    }
    segSvg+='<line x1="'+p1.x+'" y1="'+p1.y+'" x2="'+p2.x+'" y2="'+p2.y+'"'
      +' stroke="'+c+'" stroke-width="2.5" stroke-linecap="round" opacity=".9"/>';
  }

  // ── 各タスク実績点マーカー ──
  const dotsSvg=points.map(p=>{
    // 今日ラインより左（実績点X < 今日X）なら赤、右なら青
    const c=p.x < todayX ? '#DC2626' : '#2563EB';
    const hline='<line x1="'+todayX+'" y1="'+p.y+'" x2="'+p.x+'" y2="'+p.y+'"'
      +' stroke="'+c+'" stroke-width="1" stroke-dasharray="2,2" opacity=".35"/>';
    const marker=p.isOverdue&&p.x < todayX
      ? diamond(p.x, p.y, 6, c, p.label)
      : '<circle cx="'+p.x+'" cy="'+p.y+'" r="5" fill="'+c+'" stroke="#fff" stroke-width="2" opacity=".95">'
        +'<title>'+p.label+'</title></circle>';
    return hline+marker;
  }).join('');

  // ── 凡例 ──
  const legendY=totalH+ROW_H+20;
  const legendSvg=
    '<text x="8" y="'+legendY+'" font-size="10" fill="var(--accent)" font-family="DM Sans,sans-serif">◆ 始点/終点(TODAY)</text>'+
    '<text x="112" y="'+legendY+'" font-size="10" fill="#2563EB" font-family="DM Sans,sans-serif">● 進み</text>'+
    '<text x="150" y="'+legendY+'" font-size="10" fill="#DC2626" font-family="DM Sans,sans-serif">● 遅れ</text>'+
    '<text x="188" y="'+legendY+'" font-size="10" fill="#DC2626" font-family="DM Sans,sans-serif">◆ 遅延超過</text>'+
    '<text x="260" y="'+legendY+'" font-size="10" fill="var(--text3)" font-family="DM Sans,sans-serif">（完了済み・将来タスクは除外）</text>';

  const svgH=totalH+ROW_H+30;
  return '<svg id="lightning-svg"'
    +' style="position:absolute;top:0;left:0;width:100%;height:'+svgH+'px;pointer-events:none;z-index:7;overflow:visible">'
    +baselineSvg+segSvg+dotsSvg+startDiamond+endDiamond+legendSvg
    +'</svg>';
}

function toggleLightningLine(){
  showLightningLine=!showLightningLine;
  const btn=document.getElementById('lightning-btn');
  if(btn){
    btn.style.background=showLightningLine?'var(--accent)':'var(--surface)';
    btn.style.color=showLightningLine?'#fff':'var(--text3)';
    btn.style.borderColor=showLightningLine?'var(--accent)':'var(--border)';
    btn.title=showLightningLine?'イナズマ線を非表示':'イナズマ線を表示';
  }
  // チャート本体だけ再描画（ヘッダー等を保持するため）
  const scrollEl=document.getElementById('gantt-root');
  const scrollX=scrollEl?scrollEl.scrollLeft:0;
  renderGantt();
  requestAnimationFrame(()=>{const el=document.getElementById('gantt-root');if(el)el.scrollLeft=scrollX;});
}

// ── Main render ──
function renderGantt(){
  const container=document.getElementById('gantt-inner');
  const nums=calcDisplayNums();
  const treeOrder=buildTreeOrder();
  if(!treeOrder.length){
    container.innerHTML='<div class="empty-state" style="padding:60px"><div class="icon">📊</div><p>タスクがありません</p></div>';
    return;
  }

  const {minD,maxD}=ganttDateRange();
  ganttMinD=minD;

  const today=new Date(); today.setHours(0,0,0,0);

  // ── スケール列生成 ──
  const {upper,lower,cw}=buildScaleColumns(minD,maxD);
  const totalCols=lower.length;
  const totalW=totalCols*cw;
  const totalH=treeOrder.length*ROW_H;

  // 今日ラインX（スケール対応）
  const todayX=ganttScaleDateToX(today);

  // バーのX座標変換（スケール対応）
  const taskLeft=t=>ganttScaleDateToX(t.start)-cw/2;
  const taskRight=t=>ganttScaleDateToX(t.end)+cw/2;

  const GANTT_COLORS={todo:'#9B9890',doing:'#2563EB',done:'#059669',block:'#DC2626'};

  // ── Label column ──
  const conflictMap=buildConflictMap();
  const labelColHTML = treeOrder.map(t=>{
    const lvl=getLevel(t.id), padL=12+lvl*16;
    const isFolder=t.type==='folder';
    const hasCh=hasChildren(t.id);
    const isCol=collapsedSet.has(t.id);
    const icon=isFolder?(isCol||!hasCh?'📁':'📂'):'📄';
    const folderConflicts=isFolder?conflictMap.get(t.id)||[]:[];
    const folderHasConflict=folderConflicts.length>0;
    const taskConflictReasons=!isFolder?getTaskConflictReasons(t.id,conflictMap):[];
    const taskHasConflict=taskConflictReasons.length>0;
    const hasConflict=folderHasConflict||taskHasConflict;
    const bg=hasConflict
      ?'rgba(220,38,38,.04)'
      :(isFolder?'rgba(37,99,235,.03)':'var(--surface)');
    const conflictTip=folderHasConflict
      ?folderConflicts.map(c=>{const ct=tasks.find(x=>x.id===c.taskId);return(ct?ct.name:'?')+': '+c.reason;}).join('\n')
      :taskConflictReasons.join('\n');
    const warnIcon=hasConflict
      ?`<span title="${conflictTip}" style="font-size:11px;color:var(--danger);flex-shrink:0;cursor:help">⚠</span>`:'';

    const toggleBtn=hasCh
      ?`<button onclick="ganttToggleCollapse('${t.id}',event)"
          style="width:18px;height:18px;border:none;background:none;cursor:pointer;display:flex;align-items:center;justify-content:center;border-radius:3px;flex-shrink:0;color:var(--text3);padding:0;font-size:10px;transition:.1s"
          title="${isCol?'展開':'折りたたむ'}"
          onmouseover="this.style.background='var(--surface2)';this.style.color='var(--text)'"
          onmouseout="this.style.background='none';this.style.color='var(--text3)'"
        >${isCol?'▶':'▼'}</button>`
      :`<span style="width:18px;flex-shrink:0"></span>`;

    return `<div class="gantt-label-row" data-id="${t.id}"
      style="height:${ROW_H}px;padding:0 8px 0 ${padL}px;background:${bg};display:flex;align-items:center;gap:4px;border-bottom:1px solid var(--border);overflow:hidden;box-sizing:border-box;user-select:none"
      draggable="true"
      ondragstart="onDepLinkDragStart(event,'${t.id}')"
      ondragover="onDepLinkDragOver(event,'${t.id}')"
      ondragleave="onDepLinkDragLeave(event,'${t.id}')"
      ondrop="onDepLinkDrop(event,'${t.id}')">
      ${toggleBtn}
      <span style="flex-shrink:0;font-size:13px;cursor:pointer" onclick="selectTask('${t.id}')">${icon}</span>
      <span style="font-family:'DM Mono',monospace;font-size:10px;color:var(--text3);flex-shrink:0;min-width:30px;cursor:pointer" onclick="selectTask('${t.id}')">${nums[t.id]||''}</span>
      <span style="font-size:12px;font-weight:${isFolder?600:400};overflow:hidden;text-overflow:ellipsis;white-space:nowrap;flex:1;cursor:pointer" onclick="selectTask('${t.id}')">${t.name}</span>
      ${warnIcon}
      <span title="ドラッグ→別行にドロップで依存付け" style="font-size:11px;color:var(--text3);opacity:.4;cursor:grab;flex-shrink:0" class="dep-drag-handle">⇢</span>
    </div>`;
  }).join('');

  // ── Chart body cells (grid background) ──
  // (スケール対応版は buildScaleColumns 後に生成済み)

  // ── Bars (drag targets) ──
  const rowIndex={}; treeOrder.forEach((t,i)=>rowIndex[t.id]=i);
  const barsHTML = treeOrder.map((t,ri)=>{
    const taskConflictReasons=getTaskConflictReasons(t.id,conflictMap);
    const folderConflicts=t.type==='folder'?conflictMap.get(t.id)||[]:[];
    const hasConflict=taskConflictReasons.length>0||folderConflicts.length>0;
    if(!t.start||!t.end) return '<div class="gantt-bar-row" data-id="'+t.id+'"'
      +' style="position:absolute;top:'+(ri*ROW_H)+'px;left:0;width:'+totalW+'px;height:'+ROW_H+'px;pointer-events:none"></div>';
    const left=Math.max(0,taskLeft(t));
    const right=Math.min(totalW,taskRight(t));
    const width=Math.max(right-left,cw*0.3);
    const color=GANTT_COLORS[t.status]||'#9B9890';
    const pct=effectiveProgress(t); // ← フォルダは自動計算
    const barH=t.type==='folder'?14:22;
    const barTop=(ROW_H-barH)/2;
    const GRIP=6; // px width of resize handle
    return `<div class="gantt-bar-row" data-id="${t.id}"
      style="position:absolute;top:${ri*ROW_H}px;left:0;width:${totalW}px;height:${ROW_H}px">
      <!-- full-row drop zone for dep linking -->
      <div class="gantt-dep-dropzone" data-id="${t.id}"
        style="position:absolute;inset:0;z-index:1;pointer-events:none"
        ondragover="onDepLinkDragOver(event,'${t.id}')"
        ondragleave="onDepLinkDragLeave(event,'${t.id}')"
        ondrop="onDepLinkDrop(event,'${t.id}')"></div>
      <!-- bar -->
      <div class="gantt-bar" data-id="${t.id}" data-action="move"
        style="position:absolute;top:${barTop}px;left:${left}px;width:${width}px;height:${barH}px;
               border-radius:${t.type==='folder'?2:4}px;background:${color};opacity:${t.type==='folder'?.65:.88};
               overflow:visible;display:flex;align-items:center;padding:0 ${GRIP+4}px;
               box-sizing:border-box;cursor:grab;z-index:3;user-select:none;
               ${hasConflict?'box-shadow:0 0 0 2px #DC2626;':''}"
        title="${t.name}&#10;${t.start} → ${t.end}&#10;ドラッグで移動${hasConflict?'&#10;⚠ フォルダ期間との矛盾あり':''}">
        <!-- progress fill -->
        <div style="position:absolute;left:0;top:0;bottom:0;width:${pct}%;background:rgba(255,255,255,.22);pointer-events:none;border-radius:inherit"></div>
        <!-- label -->
        <span style="position:relative;z-index:1;font-size:10px;font-weight:${t.type==='folder'?600:400};color:#fff;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;pointer-events:none">${t.name.slice(0,18)}${t.name.length>18?'…':''}</span>
        <!-- left resize handle -->
        <div class="gantt-resize-handle" data-id="${t.id}" data-action="resize-left"
          style="position:absolute;left:0;top:0;width:${GRIP}px;height:100%;cursor:w-resize;z-index:4;background:rgba(0,0,0,.15);border-radius:inherit 0 0 inherit"
          title="左端ドラッグで開始日を変更"></div>
        <!-- right resize handle -->
        <div class="gantt-resize-handle" data-id="${t.id}" data-action="resize-right"
          style="position:absolute;right:0;top:0;width:${GRIP}px;height:100%;cursor:e-resize;z-index:4;background:rgba(0,0,0,.15);border-radius:0 inherit inherit 0"
          title="右端ドラッグで終了日を変更"></div>
      </div>
    </div>`;
  }).join('');

  // ── SVG dep arrows ──
  const svgPaths=[];
  treeOrder.forEach((t,ri)=>{
    if(!t.deps||!t.deps.length||!t.start)return;
    const toX=taskLeft(t), toY=ri*ROW_H+ROW_H/2;
    t.deps.forEach(depId=>{
      const pred=tasks.find(x=>x.id===depId);
      if(!pred||!pred.end)return;
      const fromX=taskRight(pred), fromRI=rowIndex[pred.id];
      if(fromRI===undefined)return;
      const fromY=fromRI*ROW_H+ROW_H/2;
      const midX=Math.max(fromX+8,toX-8);
      const overlap = pred.end && t.start && s2d(pred.end) >= s2d(t.start);
      svgPaths.push({
        path:'M'+fromX+','+fromY+' L'+midX+','+fromY+' L'+midX+','+toY+' L'+toX+','+toY,
        fromId:pred.id, toId:t.id, overlap
      });
    });
  });
  // ── SVG dep arrows ──
  const svgArrowPaths = svgPaths.map(p=>{
    if(p.overlap){
      return '<path class="dep-arrow dep-arrow-overlap"'
        +' data-from="'+p.fromId+'" data-to="'+p.toId+'" d="'+p.path+'"'
        +' fill="none" stroke="#DC2626" stroke-width="2" stroke-dasharray="5,3" opacity=".9"'
        +' marker-end="url(#arr-overlap)">'
        +'<title>⚠ 期間重複：前工程の終了前に後工程が開始されています</title>'
        +'</path>';
    } else {
      return '<path class="dep-arrow"'
        +' data-from="'+p.fromId+'" data-to="'+p.toId+'" d="'+p.path+'"'
        +' fill="none" stroke="#64748B" stroke-width="1.5" stroke-dasharray="5,3" opacity=".75"'
        +' marker-end="url(#arr)"/>';
    }
  }).join('');

  const svgHTML='<svg id="gantt-svg" style="position:absolute;top:0;left:0;width:'+totalW+'px;height:'+totalH+'px;pointer-events:none;z-index:5;overflow:visible">'
    +'<defs>'
    +'<marker id="arr" markerWidth="7" markerHeight="7" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 Z" fill="#64748B" opacity=".9"/></marker>'
    +'<marker id="arr-overlap" markerWidth="7" markerHeight="7" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 Z" fill="#DC2626"/></marker>'
    +'<marker id="arr-new" markerWidth="7" markerHeight="7" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 Z" fill="var(--accent)"/></marker>'
    +'</defs>'
    +svgArrowPaths
    +'<path id="dep-link-preview" d="" fill="none" stroke="var(--accent)" stroke-width="2" stroke-dasharray="6,3" opacity="0" marker-end="url(#arr-new)"/>'
    +'</svg>';

  // ── Today line ──
  const todayHTML=
    '<div style="position:absolute;top:0;bottom:0;left:'+todayX+'px;width:2px;background:var(--accent);opacity:.7;z-index:6;pointer-events:none"></div>'+
    '<div style="position:absolute;top:-8px;left:'+(todayX-19)+'px;width:40px;background:var(--accent);color:#fff;font-size:9px;font-weight:700;text-align:center;border-radius:3px;padding:2px 0;z-index:6;pointer-events:none">TODAY</div>';

  // ── Tooltip ──
  const tooltipHTML='<div id="gantt-tooltip" style="display:none;position:fixed;background:var(--text);color:#fff;font-size:11px;padding:5px 10px;border-radius:5px;pointer-events:none;z-index:999;white-space:nowrap;font-family:DM Mono,monospace"></div>';

  // ── ヘッダー HTML（スケール対応） ──
  const upperHeaderHTML=upper.map(u=>{
    const w=u.count*cw;
    return '<div style="flex:0 0 '+w+'px;height:'+HDR_MONTH+'px;line-height:'+HDR_MONTH+'px;'
      +'font-size:11px;font-weight:600;color:var(--text2);text-align:center;'
      +'border-left:1px solid var(--border);border-bottom:1px solid var(--border);'
      +'background:var(--surface2);box-sizing:border-box;overflow:hidden;white-space:nowrap">'
      +u.label+'</div>';
  }).join('');

  const lowerHeaderHTML=lower.map(col=>{
    const dc=col.isTdy?'var(--accent)':col.isWk?'var(--danger)':'var(--text3)';
    const bg=col.isTdy?'var(--accent-light)':col.isWk?'#FAFAF8':'var(--surface2)';
    const fw=col.isTdy?700:400;
    return '<div style="flex:0 0 '+cw+'px;height:'+HDR_DAY+'px;line-height:'+HDR_DAY+'px;'
      +'font-size:9px;text-align:center;border-left:1px solid var(--border);'
      +'border-bottom:2px solid var(--border);color:'+dc+';font-weight:'+fw+';'
      +'background:'+bg+';box-sizing:border-box;overflow:hidden;white-space:nowrap">'
      +col.label+'</div>';
  }).join('');

  // ── グリッド（列背景） ──
  const gridHTML=lower.map((col,ci)=>{
    const bg=col.isTdy?'rgba(37,99,235,.06)':col.isWk?'rgba(0,0,0,.025)':'transparent';
    return '<div style="position:absolute;top:0;bottom:0;left:'+(ci*cw)+'px;width:'+cw+'px;'
      +'border-left:1px solid var(--border);background:'+bg+';box-sizing:border-box"></div>';
  }).join('');

  const rowDivHTML=treeOrder.map((_,ri)=>'<div style="position:absolute;top:'+(((ri+1)*ROW_H)-1)+'px;left:0;right:0;height:1px;background:var(--border)"></div>').join('');

  container.innerHTML=
    tooltipHTML+
    // 単一スクロールコンテナ（縦横両方向スクロール）
    '<div id="gantt-root" style="flex:1;min-height:0;overflow:auto;border:1px solid var(--border);border-radius:var(--radius);background:var(--surface);position:relative">'+
      // ── ヘッダー行（縦スクロールで上固定） ──
      '<div style="display:flex;position:sticky;top:0;z-index:30;min-width:max-content">'+
        // 交差点：タスク名ヘッダー（縦横両方固定）
        '<div style="position:sticky;left:0;z-index:40;flex:0 0 '+LABEL_W+'px;min-width:'+LABEL_W+'px;background:var(--surface2);border-right:2px solid var(--border);border-bottom:2px solid var(--border);display:flex;flex-direction:column">'+
          // 上段ヘッダーの高さ分（上位スケール行）
          '<div style="height:'+HDR_MONTH+'px;border-bottom:1px solid var(--border)"></div>'+
          // 下段：展開/折りたたみボタン
          '<div style="height:'+HDR_DAY+'px;display:flex;align-items:center;padding:0 10px;gap:6px;font-size:11px;font-weight:600;text-transform:uppercase;letter-spacing:.06em;color:var(--text3)">'+
            '<button onclick="ganttExpandAll()" title="全展開" style="width:20px;height:20px;border:1px solid var(--border);border-radius:3px;background:var(--surface);cursor:pointer;font-size:11px;display:flex;align-items:center;justify-content:center;flex-shrink:0;color:var(--text3)">▼</button>'+
            '<button onclick="ganttCollapseAll()" title="全折りたたみ" style="width:20px;height:20px;border:1px solid var(--border);border-radius:3px;background:var(--surface);cursor:pointer;font-size:11px;display:flex;align-items:center;justify-content:center;flex-shrink:0;color:var(--text3)">▶</button>'+
            '<span style="font-family:DM Mono,monospace;margin-right:2px;font-size:10px">No</span><span style="font-size:10px">タスク名</span>'+
            '<span style="margin-left:auto;font-size:9px;color:var(--text3);font-weight:400;letter-spacing:0;text-transform:none">⇢依存付け</span>'+
          '</div>'+
        '</div>'+
        // カレンダーヘッダー（横スクロールと一緒に動く）
        '<div style="flex:1;display:flex;flex-direction:column;min-width:'+totalW+'px">'+
          '<div style="display:flex;min-width:'+totalW+'px">'+upperHeaderHTML+'</div>'+
          '<div style="display:flex;min-width:'+totalW+'px;border-bottom:2px solid var(--border)">'+lowerHeaderHTML+'</div>'+
        '</div>'+
      '</div>'+
      // ── 本体行（タスク名列 sticky left + チャート本体） ──
      '<div style="display:flex;min-width:max-content">'+
        // タスク名列（横スクロールで左固定）
        '<div id="gantt-labels" style="position:sticky;left:0;z-index:20;flex:0 0 '+LABEL_W+'px;min-width:'+LABEL_W+'px;border-right:2px solid var(--border);background:var(--surface)">'+
          '<div id="gantt-label-body">'+labelColHTML+'</div>'+
        '</div>'+
        // チャート本体
        '<div id="gantt-chart-scroll" style="flex:1;min-width:'+totalW+'px;position:relative">'+
          '<div id="gantt-body" style="position:relative;min-width:'+totalW+'px;height:'+totalH+'px">'+
            gridHTML+rowDivHTML+barsHTML+svgHTML+todayHTML+
            (showLightningLine ? buildLightningLineHTML(treeOrder, totalH) : '')+
          '</div>'+
        '</div>'+
      '</div>'+
    '</div>';

  // attach bar drag events
  attachGanttDragEvents();

  // 初回表示時はTodayを中央にスクロール
  if(_ganttFirstRender){
    _ganttFirstRender=false;
    requestAnimationFrame(()=>{
      const el=document.getElementById('gantt-root');
      if(!el) return;
      const tx=ganttScaleDateToX(new Date());
      el.scrollLeft=Math.max(0, tx - el.clientWidth/2);
    });
  }
}

// ════════════════════════════════════════════════════
// BAR DRAG: move + resize-left + resize-right
// ════════════════════════════════════════════════════
function attachGanttDragEvents(){
  const body=document.getElementById('gantt-body');
  if(!body)return;

  body.addEventListener('mousedown', e=>{
    const handle=e.target.closest('[data-action]');
    if(!handle)return;
    const action=handle.dataset.action;
    const id=handle.dataset.id;
    const t=tasks.find(x=>x.id===id);
    if(!t||!t.start||!t.end)return;
    e.preventDefault();
    e.stopPropagation();

    const startOffX=e.clientX;
    const origStart=s2d(t.start), origEnd=s2d(t.end);
    const origDur=Math.round((origEnd-origStart)/86400000);

    ganttDragState={id,action,startOffX,origStart,origEnd,origDur,moved:false};
    document.body.style.userSelect='none';
    document.body.style.cursor=action==='move'?'grabbing':action==='resize-left'?'w-resize':'e-resize';
    showTooltip(action==='move'?`移動中: ${d2s(origStart)} → ${d2s(origEnd)}`:`リサイズ中`);
  });

  document.addEventListener('mousemove', onGanttMouseMove);
  document.addEventListener('mouseup',   onGanttMouseUp);
}

function onGanttMouseMove(e){
  if(!ganttDragState)return;
  const {id,action,startOffX,origStart,origEnd,origDur}=ganttDragState;
  const t=tasks.find(x=>x.id===id);
  if(!t)return;

  const dx=e.clientX-startOffX;
  const deltaDays=Math.round(dx/DAY_W);
  if(deltaDays!==0)ganttDragState.moved=true;

  let newStart=origStart, newEnd=origEnd;
  if(action==='move'){
    newStart=addDays(origStart,deltaDays);
    newEnd=addDays(origStart,deltaDays+origDur);
  } else if(action==='resize-left'){
    newStart=addDays(origStart,deltaDays);
    if(newStart>=newEnd)newStart=addDays(newEnd,-1);
  } else if(action==='resize-right'){
    newEnd=addDays(origEnd,deltaDays);
    if(newEnd<=newStart)newEnd=addDays(newStart,1);
  }

  // live-update bar DOM
  const bar=document.querySelector(`.gantt-bar[data-id="${id}"]`);
  if(bar){
    const left=dateToOff(newStart)*DAY_W;
    const right=(dateToOff(newEnd)+1)*DAY_W;
    const width=Math.max(right-left,DAY_W);
    bar.style.left=left+'px';
    bar.style.width=width+'px';
  }
  // update dep arrows live
  updateDepArrows(id, newStart, newEnd);
  showTooltip(`${d2s(newStart)} → ${d2s(newEnd)} (${Math.round((newEnd-newStart)/86400000)+1}日間)`);
}

function onGanttMouseUp(e){
  if(!ganttDragState)return;
  const {id,action,startOffX,origStart,origEnd,origDur,moved}=ganttDragState;
  ganttDragState=null;
  document.body.style.userSelect='';
  document.body.style.cursor='';
  hideTooltip();

  if(!moved)return;

  const dx=e.clientX-startOffX;
  const deltaDays=Math.round(dx/DAY_W);
  const t=tasks.find(x=>x.id===id);
  if(!t)return;

  if(action==='move'){
    t.start=d2s(addDays(origStart,deltaDays));
    t.end=d2s(addDays(origStart,deltaDays+origDur));
  } else if(action==='resize-left'){
    let ns=addDays(origStart,deltaDays);
    if(ns>=s2d(t.end))ns=addDays(s2d(t.end),-1);
    t.start=d2s(ns);
  } else if(action==='resize-right'){
    let ne=addDays(origEnd,deltaDays);
    if(ne<=s2d(t.start))ne=addDays(s2d(t.start),1);
    t.end=d2s(ne);
  }

  // re-render to sync list panel dates too
  renderAll();
}

function updateDepArrows(movingId, newStart, newEnd){
  const svg=document.getElementById('gantt-svg');
  if(!svg)return;
  const treeOrder=buildTreeOrder();
  const rowIndex={};treeOrder.forEach((t,i)=>rowIndex[t.id]=i);

  svg.querySelectorAll('.dep-arrow').forEach(path=>{
    const fromId=path.dataset.from, toId=path.dataset.to;
    const fromT=fromId===movingId?{end:d2s(newEnd)}:tasks.find(x=>x.id===fromId);
    const toT  =toId  ===movingId?{start:d2s(newStart)}:tasks.find(x=>x.id===toId);
    if(!fromT||!toT||!fromT.end||!toT.start)return;
    const fromRI=rowIndex[fromId],toRI=rowIndex[toId];
    if(fromRI===undefined||toRI===undefined)return;
    const fromX=(dateToOff(fromT.end)+1)*DAY_W, fromY=fromRI*ROW_H+ROW_H/2;
    const toX  =dateToOff(toT.start)*DAY_W,     toY  =toRI  *ROW_H+ROW_H/2;
    const midX=Math.max(fromX+8,toX-8);
    path.setAttribute('d',`M${fromX},${fromY} L${midX},${fromY} L${midX},${toY} L${toX},${toY}`);

    // live overlap check
    const overlap = s2d(fromT.end) >= s2d(toT.start);
    if(overlap){
      path.setAttribute('stroke','#DC2626');
      path.setAttribute('stroke-width','2');
      path.setAttribute('opacity','0.9');
      path.setAttribute('marker-end','url(#arr-overlap)');
      path.classList.add('dep-arrow-overlap');
    } else {
      path.setAttribute('stroke','#64748B');
      path.setAttribute('stroke-width','1.5');
      path.setAttribute('opacity','0.75');
      path.setAttribute('marker-end','url(#arr)');
      path.classList.remove('dep-arrow-overlap');
    }
  });
}

// ════════════════════════════════════════════════════
// DEPENDENCY LINK DRAG (label rows + chart dropzones)
// ════════════════════════════════════════════════════
function onDepLinkDragStart(e, fromId){
  // only trigger on the ⇢ handle or label row itself
  ganttDepLinkState={fromId};
  e.dataTransfer.effectAllowed='link';
  e.dataTransfer.setData('text/plain', fromId);
  // make drag ghost minimal
  const ghost=document.createElement('div');
  ghost.style.cssText='position:fixed;top:-100px;left:-100px;width:60px;height:24px;background:var(--accent);color:#fff;border-radius:4px;display:flex;align-items:center;justify-content:center;font-size:11px';
  ghost.textContent='依存リンク';
  document.body.appendChild(ghost);
  e.dataTransfer.setDragImage(ghost,30,12);
  setTimeout(()=>ghost.remove(),0);
  // enable all dropzones
  document.querySelectorAll('.gantt-dep-dropzone').forEach(el=>el.style.pointerEvents='all');
}

function onDepLinkDragOver(e, targetId){
  if(!ganttDepLinkState)return;
  const {fromId}=ganttDepLinkState;
  if(targetId===fromId)return;
  e.preventDefault();
  e.dataTransfer.dropEffect='link';

  // highlight target row
  if(ganttHoverDepTarget!==targetId){
    clearDepLinkHighlight();
    ganttHoverDepTarget=targetId;
    document.querySelectorAll(`.gantt-label-row[data-id="${targetId}"], .gantt-bar-row[data-id="${targetId}"]`).forEach(el=>{
      el.style.outline='2px dashed var(--accent)';
      el.style.outlineOffset='-2px';
    });
  }
  // draw preview arrow
  drawDepPreview(fromId, targetId);
}

function onDepLinkDragLeave(e, targetId){
  // only clear if leaving to outside
  if(e.relatedTarget&&e.currentTarget.contains(e.relatedTarget))return;
  if(ganttHoverDepTarget===targetId){
    clearDepLinkHighlight();
    ganttHoverDepTarget=null;
    const preview=document.getElementById('dep-link-preview');
    if(preview)preview.setAttribute('opacity','0');
  }
}

function onDepLinkDrop(e, targetId){
  e.preventDefault();
  const fromId=ganttDepLinkState?.fromId||e.dataTransfer.getData('text/plain');
  ganttDepLinkState=null;
  ganttHoverDepTarget=null;
  clearDepLinkHighlight();
  document.querySelectorAll('.gantt-dep-dropzone').forEach(el=>el.style.pointerEvents='none');

  if(!fromId||fromId===targetId)return;

  const target=tasks.find(x=>x.id===targetId);
  if(!target)return;
  if(!target.deps)target.deps=[];
  if(target.deps.includes(fromId)){
    // already linked → offer to remove
    if(confirm(`依存関係 ${calcDisplayNums()[fromId]||fromId} → ${calcDisplayNums()[targetId]||targetId} を削除しますか？`)){
      target.deps=target.deps.filter(d=>d!==fromId);
      renderAll();
    }
    return;
  }
  target.deps.push(fromId);
  renderAll();
}

function drawDepPreview(fromId, toId){
  const svg=document.getElementById('gantt-svg');
  const preview=document.getElementById('dep-link-preview');
  if(!svg||!preview)return;
  const treeOrder=buildTreeOrder();
  const rowIndex={};treeOrder.forEach((t,i)=>rowIndex[t.id]=i);
  const fromT=tasks.find(x=>x.id===fromId), toT=tasks.find(x=>x.id===toId);
  const fromRI=rowIndex[fromId], toRI=rowIndex[toId];
  if(fromRI===undefined||toRI===undefined)return;
  const fromX=fromT?.end?(dateToOff(fromT.end)+1)*DAY_W:DAY_W;
  const toX=toT?.start?dateToOff(toT.start)*DAY_W:0;
  const fromY=fromRI*ROW_H+ROW_H/2, toY=toRI*ROW_H+ROW_H/2;
  const midX=Math.max(fromX+8,toX-8);
  preview.setAttribute('d',`M${fromX},${fromY} L${midX},${fromY} L${midX},${toY} L${toX},${toY}`);
  preview.setAttribute('opacity','1');
}

function clearDepLinkHighlight(){
  document.querySelectorAll('.gantt-label-row,.gantt-bar-row').forEach(el=>{
    el.style.outline=''; el.style.outlineOffset='';
  });
}

// ════════════════════════════════════════════════════
// ROW SORT DRAG  (sort mode) + DEP LINK DRAG (dep mode)
// ════════════════════════════════════════════════════
let sortModeOn=false;
let _dragId=null;       // id being dragged
let _dragOverId=null;   // id being hovered
let _dropPos='below';   // 'above' | 'below' | 'child'

function toggleSortMode(){
  sortModeOn=!sortModeOn;
  const btn=document.getElementById('sort-toggle-btn');
  btn.classList.toggle('active',sortModeOn);
  btn.textContent=sortModeOn?'⠿ 並替中 (ON)':'⠿ 並替モード';
  const wbs=document.getElementById('list-view');
  wbs.classList.toggle('sort-mode-active',sortModeOn);
  // hint
  if(sortModeOn){
    const hint=document.getElementById('sort-mode-hint');
    if(hint)hint.style.display='flex';
  }else{
    const hint=document.getElementById('sort-mode-hint');
    if(hint)hint.style.display='none';
  }
}

// ── Unified drag start (route to sort vs dep) ──
function onRowDragStart(e, id){
  if(sortModeOn){
    // only start if dragging handle area or sort mode on
    _dragId=id;
    e.dataTransfer.effectAllowed='move';
    e.dataTransfer.setData('text/plain',id);
    // ghost
    const row=e.currentTarget;
    setTimeout(()=>row.classList.add('dragging'),0);
  } else {
    // dep link mode
    ganttDepLinkState={fromId:id};
    e.dataTransfer.effectAllowed='link';
    e.dataTransfer.setData('text/plain',id);
  }
}

function onRowDragOver(e, id){
  e.preventDefault();
  if(sortModeOn){
    if(!_dragId||_dragId===id)return;
    _dragOverId=id;
    // determine above/below/child from mouse Y position in row
    const row=e.currentTarget;
    const rect=row.getBoundingClientRect();
    const relY=(e.clientY-rect.top)/rect.height;
    const dragLvl=getLevel(_dragId);
    const overLvl=getLevel(id);
    if(relY<0.25) _dropPos='above';
    else if(relY>0.75) _dropPos='below';
    else _dropPos='child'; // middle zone → make child
    // visual feedback
    clearRowDropFeedback();
    row.classList.add(_dropPos==='above'?'drag-over-above':'drag-over-below');
    e.dataTransfer.dropEffect='move';
  } else {
    // dep link hover
    e.dataTransfer.dropEffect='link';
    if(ganttHoverDepTarget!==id){
      clearDepLinkHighlight();
      ganttHoverDepTarget=id;
      document.querySelectorAll(`.task-row[data-id="${id}"]`).forEach(el=>{
        el.style.outline='2px dashed var(--accent)';
        el.style.outlineOffset='-2px';
      });
    }
  }
}

function onRowDragLeave(e, id){
  if(sortModeOn){
    const row=e.currentTarget;
    if(!row.contains(e.relatedTarget)) row.classList.remove('drag-over-above','drag-over-below');
  } else {
    if(ganttHoverDepTarget===id){
      clearDepLinkHighlight();
      ganttHoverDepTarget=null;
    }
  }
}

function onRowDrop(e, id){
  e.preventDefault();
  if(sortModeOn){
    clearRowDropFeedback();
    if(!_dragId||_dragId===id){_dragId=null;return;}
    applySort(_dragId, id, _dropPos);
    _dragId=null;_dragOverId=null;
  } else {
    onListDepDrop(e, id);
  }
}

function onRowDragEnd(e){
  clearRowDropFeedback();
  document.querySelectorAll('.task-row.dragging').forEach(r=>r.classList.remove('dragging'));
  _dragId=null;_dragOverId=null;
}

function clearRowDropFeedback(){
  document.querySelectorAll('.task-row.drag-over-above,.task-row.drag-over-below')
    .forEach(r=>r.classList.remove('drag-over-above','drag-over-below'));
}

// ── Core sort logic ──
function applySort(dragId, targetId, pos){
  const dragTask=tasks.find(t=>t.id===dragId);
  const targetTask=tasks.find(t=>t.id===targetId);
  if(!dragTask||!targetTask)return;

  // gather dragTask subtree (drag node + all descendants)
  function subtree(id){
    const res=[id];
    tasks.filter(t=>t.parentId===id).forEach(c=>subtree(c.id).forEach(x=>res.push(x)));
    return res;
  }
  const dragSubtreeIds=subtree(dragId);

  // guard: can't drop inside own subtree
  if(dragSubtreeIds.includes(targetId))return;

  // remove drag subtree from tasks array
  const dragSubtree=dragSubtreeIds.map(sid=>tasks.find(t=>t.id===sid));
  tasks=tasks.filter(t=>!dragSubtreeIds.includes(t.id));

  // update parentId of drag root
  if(pos==='child'){
    dragTask.parentId=targetId;
  } else {
    dragTask.parentId=targetTask.parentId; // same level as target
  }

  // find insertion index in tasks array
  let insertIdx;
  if(pos==='child'){
    // insert after all current children of target (append as last child)
    const lastChildIdx=tasks.reduce((acc,t,i)=>t.parentId===targetId?i:acc,-1);
    insertIdx=lastChildIdx>=0?lastChildIdx+1:tasks.findIndex(t=>t.id===targetId)+1;
  } else if(pos==='above'){
    insertIdx=tasks.findIndex(t=>t.id===targetId);
    if(insertIdx<0)insertIdx=tasks.length;
  } else { // below
    // insert after target and its entire subtree
    const targetSub=subtree(targetId); // already re-computed on stripped array; need full walk
    // find last index of target subtree in current tasks
    let lastIdx=tasks.findIndex(t=>t.id===targetId);
    for(let i=lastIdx+1;i<tasks.length;i++){
      if(isDescendantOf(tasks[i].id,targetId)) lastIdx=i; else break;
    }
    insertIdx=lastIdx+1;
  }
  if(insertIdx<0)insertIdx=tasks.length;

  tasks.splice(insertIdx,0,...dragSubtree);
  renderAll();
}

function isDescendantOf(id,ancestorId){
  let cur=tasks.find(t=>t.id===id);
  while(cur&&cur.parentId){
    if(cur.parentId===ancestorId)return true;
    cur=tasks.find(t=>t.id===cur.parentId);
  }
  return false;
}

// ── list dep drag (non-sort mode) ──
function onListDepDragStart(e, fromId){
  ganttDepLinkState={fromId};
  e.dataTransfer.effectAllowed='link';
  e.dataTransfer.setData('text/plain',fromId);
}
function onListDepDrop(e, targetId){
  e.preventDefault();
  const fromId=ganttDepLinkState?.fromId||e.dataTransfer.getData('text/plain');
  ganttDepLinkState=null;
  ganttHoverDepTarget=null;
  clearDepLinkHighlight();
  document.querySelectorAll('.task-row').forEach(r=>{r.style.outline='';r.style.outlineOffset='';});
  if(!fromId||fromId===targetId)return;
  const target=tasks.find(x=>x.id===targetId);
  if(!target)return;
  if(!target.deps)target.deps=[];
  if(target.deps.includes(fromId)){
    if(confirm(`依存関係 ${calcDisplayNums()[fromId]||fromId} → ${calcDisplayNums()[targetId]||targetId} を削除しますか？`)){
      target.deps=target.deps.filter(d=>d!==fromId);renderAll();
    }
    return;
  }
  target.deps.push(fromId);
  renderAll();
}

// ── Tooltip ──
function showTooltip(text){
  const tt=document.getElementById('gantt-tooltip');
  if(!tt)return;
  tt.textContent=text; tt.style.display='block';
  document.addEventListener('mousemove',moveTooltip);
}
function moveTooltip(e){
  const tt=document.getElementById('gantt-tooltip');
  if(tt){tt.style.left=(e.clientX+14)+'px';tt.style.top=(e.clientY-28)+'px';}
}
function hideTooltip(){
  const tt=document.getElementById('gantt-tooltip');
  if(tt)tt.style.display='none';
  document.removeEventListener('mousemove',moveTooltip);
}


// ─── Stats ───
// ── フォルダ日程矛盾の検知ユーティリティ ──
// フォルダの全子孫タスクを取得
function getAllDescendants(folderId){
  const result=[];
  const walk=id=>{tasks.filter(t=>t.parentId===id).forEach(t=>{result.push(t);walk(t.id);});};
  walk(folderId);
  return result;
}
// フォルダ1件の矛盾を検査 → 矛盾している子孫IDの配列を返す
function getFolderConflicts(folder){
  if(!folder.start&&!folder.end)return[];
  const conflicts=[];
  getAllDescendants(folder.id).forEach(t=>{
    if(!t.start&&!t.end)return;
    let reason=null;
    if(folder.start&&t.start&&s2d(t.start)<s2d(folder.start))
      reason=`開始日 ${t.start} がフォルダ開始日 ${folder.start} より前`;
    if(folder.end&&t.end&&s2d(t.end)>s2d(folder.end))
      reason=`終了日 ${t.end} がフォルダ終了日 ${folder.end} を超過`;
    if(folder.end&&t.start&&s2d(t.start)>s2d(folder.end))
      reason=`開始日 ${t.start} がフォルダ終了日 ${folder.end} を超過`;
    if(reason)conflicts.push({taskId:t.id,reason});
  });
  return conflicts;
}
// 全フォルダの矛盾をまとめて返す → Map<folderId, conflicts[]>
function buildConflictMap(){
  const map=new Map();
  tasks.filter(t=>t.type==='folder').forEach(f=>{
    const c=getFolderConflicts(f);
    if(c.length)map.set(f.id,c);
  });
  return map;
}
// タスクIDが何らかの矛盾に関与しているか（子孫として）
function getTaskConflictReasons(taskId, conflictMap){
  const reasons=[];
  conflictMap.forEach((conflicts,folderId)=>{
    const hit=conflicts.find(c=>c.taskId===taskId);
    if(hit){
      const f=tasks.find(t=>t.id===folderId);
      reasons.push(`📁${f?f.name:'フォルダ'}: ${hit.reason}`);
    }
  });
  return reasons;
}

function updateStats(){
  const allLeaf=tasks.filter(t=>!hasChildren(t.id));
  const done=allLeaf.filter(t=>t.status==='done').length;
  const today=new Date();today.setHours(0,0,0,0);
  const overdue=tasks.filter(t=>t.end&&new Date(t.end)<today&&t.status!=='done').length;
  // 矛盾件数（フォルダ単位でカウント）
  const conflictMap=buildConflictMap();
  const conflictCount=conflictMap.size;

  document.getElementById('stat-total').textContent=tasks.length;
  document.getElementById('stat-done').textContent=done;
  document.getElementById('stat-overdue').textContent=overdue;
  const pct=allLeaf.length?Math.round(done/allLeaf.length*100):0;
  document.getElementById('stat-bar').style.width=pct+'%';
  document.getElementById('stat-total-mini').textContent=tasks.length;
  document.getElementById('stat-done-mini').textContent=done;
  document.getElementById('stat-overdue-mini').textContent=overdue;

  // 矛盾カード
  const conflictCard=document.getElementById('conflict-stat-card');
  if(conflictCard){
    conflictCard.style.display=conflictCount>0?'block':'none';
    const el=document.getElementById('stat-conflict');
    if(el)el.textContent=conflictCount;
  }

  const assignees=[...new Set(tasks.map(t=>t.assignee).filter(Boolean))];
  document.getElementById('assignee-legend').innerHTML=assignees.map(a=>`<div class="legend-item"><div class="avatar" style="background:${getAssigneeColor(a)};width:20px;height:20px;font-size:9px">${a.split(' ').map(w=>w[0]).join('').slice(0,2).toUpperCase()}</div>${a}</div>`).join('');
}

function updateAssigneeFilter(){
  const sel=document.getElementById('filter-assignee');
  const cur=sel.value;
  const assignees=[...new Set(tasks.map(t=>t.assignee).filter(Boolean))];
  sel.innerHTML=`<option value="">全担当者</option>`+assignees.map(a=>`<option value="${a}">${a}</option>`).join('');
  sel.value=cur;
}

// ─── Actions ───
function toggleCollapse(id,e){e.stopPropagation();collapsedSet.has(id)?collapsedSet.delete(id):collapsedSet.add(id);renderAll();}
function expandAll(){collapsedSet.clear();renderAll();}
function collapseAll(){tasks.filter(t=>hasChildren(t.id)).forEach(t=>collapsedSet.add(t.id));renderAll();}

function selectTask(id){
  selectedTaskId=id;
  const t=tasks.find(x=>x.id===id);if(!t)return;
  const nums=calcDisplayNums();
  document.getElementById('dp-title').textContent=t.name;
  document.getElementById('dp-id').textContent=`No ${nums[id]||id} · ${t.type==='folder'?'📁 フォルダ':'📄 タスク'}`;
  document.getElementById('dp-name').value=t.name;
  document.getElementById('dp-deliverable').value=t.deliverable||'';
  document.getElementById('dp-note').value=t.note||'';
  // 日付を YYYY-MM-DD に正規化してセット
  const normDate=v=>{
    if(!v) return '';
    const s=String(v).trim();
    // YYYY-MM-DD 形式かチェック
    if(/^\d{4}-\d{2}-\d{2}$/.test(s)) return s;
    // それ以外はDateオブジェクト経由で変換を試みる
    try{
      const d=new Date(s);
      if(isNaN(d.getTime())) return '';
      return d.toISOString().slice(0,10);
    }catch(e){ return ''; }
  };
  document.getElementById('dp-start').value=normDate(t.start);
  document.getElementById('dp-end').value=normDate(t.end);
  setAssigneeField('dp', t.assignee||'');
  document.getElementById('dp-status').value=t.status;
  document.getElementById('dp-progress').value=t.progress||0;
  document.getElementById('dp-prog-val').textContent=t.progress||0;
  document.getElementById('dp-deps').value=(t.deps||[]).map(d=>{const nums2=calcDisplayNums();return nums2[d]||d;}).join(', ');
  document.getElementById('dp-type').value=t.type||'task';
  document.getElementById('detail-panel').classList.add('open');
  renderList();
}

function dpUpdate(field,val){
  const t=tasks.find(x=>x.id===selectedTaskId);if(!t)return;
  t[field]=val;
  if(field==='name')document.getElementById('dp-title').textContent=val;
  renderAll();
}

function dpUpdateDeps(val){
  // resolve display numbers back to internal IDs
  const nums=calcDisplayNums();
  const numToId={};Object.entries(nums).forEach(([id,n])=>numToId[n]=id);
  const t=tasks.find(x=>x.id===selectedTaskId);if(!t)return;
  t.deps=val.split(',').map(s=>s.trim()).filter(Boolean).map(s=>numToId[s]||s);
  renderAll();
}

function closeDetail(){selectedTaskId=null;document.getElementById('detail-panel').classList.remove('open');renderList();}

function deleteTask(id,e){
  if(e)e.stopPropagation();
  if(!confirm('このアイテムと子アイテムをすべて削除しますか？'))return;
  const toDelete=[id];
  const collect=pid=>{tasks.filter(t=>t.parentId===pid).forEach(t=>{toDelete.push(t.id);collect(t.id);});};
  collect(id);
  tasks=tasks.filter(t=>!toDelete.includes(t.id));
  if(toDelete.includes(selectedTaskId))closeDetail();
  renderAll();
}
function deleteSelectedTask(){deleteTask(selectedTaskId,null);}

// ─── Add Modal ───
let addParentId=null;
function openAddModal(parentId,e){
  if(e){e.stopPropagation();e.preventDefault();}
  addParentId=parentId||null;

  const sel=document.getElementById('m-parent');
  const nums=calcDisplayNums();
  const buildIndent=id=>{let d=0,c=tasks.find(t=>t.id===id);while(c&&c.parentId){d++;c=tasks.find(t=>t.id===c.parentId);}return'　'.repeat(d);};
  sel.innerHTML='<option value="">なし（最上位）</option>'+tasks.map(t=>`<option value="${t.id}">${buildIndent(t.id)}${nums[t.id]} ${t.name}</option>`).join('');
  sel.value=addParentId||'';

  const banner=document.getElementById('modal-parent-banner');
  const toplevel=document.getElementById('modal-toplevel-banner');
  const titleEl=document.getElementById('modal-title-text');

  if(addParentId){
    const buildPath=id=>{const parts=[];let cur=tasks.find(t=>t.id===id);while(cur){parts.unshift(`${nums[cur.id]} ${cur.name}`);cur=tasks.find(t=>t.id===cur.parentId);}return parts.join(' › ');};
    document.getElementById('modal-parent-label').textContent=buildPath(addParentId);
    banner.style.display='block';toplevel.style.display='none';
    titleEl.textContent='子アイテムを追加';
  }else{
    banner.style.display='none';toplevel.style.display='block';
    titleEl.textContent='最上位アイテムを追加';
  }

  document.getElementById('m-name').value='';
  document.getElementById('m-deliverable').value='';
  document.getElementById('m-type').value='task';
  document.getElementById('m-status').value='todo';
  // pre-fill assignee with current logged-in user
  const cu=currentUser();
  setAssigneeField('m', cu?cu.name:'');
  // 親タスクの開始日・終了日を継承（設定されている場合のみ）
  const parentTask=addParentId?tasks.find(t=>t.id===addParentId):null;
  document.getElementById('m-start').value=parentTask?.start||'';
  document.getElementById('m-end').value=parentTask?.end||'';
  document.getElementById('m-progress').value=0;
  document.getElementById('m-deps').value='';
  document.getElementById('m-note').value='';

  sel.onchange=()=>{addParentId=sel.value||null;openAddModal(addParentId,null);document.getElementById('add-modal').classList.add('open');};
  document.getElementById('add-modal').classList.add('open');
  setTimeout(()=>document.getElementById('m-name').focus(),100);
}
function closeAddModal(){document.getElementById('add-modal').classList.remove('open');}

function submitAddTask(){
  const name=document.getElementById('m-name').value.trim();
  if(!name){alert('名前を入力してください');return;}
  const pId=document.getElementById('m-parent').value||null;
  const type=document.getElementById('m-type').value;
  const nums=calcDisplayNums();
  const numToId={};Object.entries(nums).forEach(([id,n])=>numToId[n]=id);
  const deps=document.getElementById('m-deps').value.split(',').map(s=>s.trim()).filter(Boolean).map(s=>numToId[s]||s);
  tasks.push({
    id:uid(), parentId:pId, type,
    name, deliverable:document.getElementById('m-deliverable').value,
    status:document.getElementById('m-status').value,
    assignee:document.getElementById('m-assignee').value,
    start:document.getElementById('m-start').value||null,
    end:document.getElementById('m-end').value||null,
    progress:parseInt(document.getElementById('m-progress').value)||0,
    deps, note:document.getElementById('m-note').value
  });
  closeAddModal();renderAll();
}

// ─── Context Menu ───
let ctxTargetId=null;
function openCtxMenu(e,taskId){
  e.preventDefault();e.stopPropagation();
  ctxTargetId=taskId;
  const t=tasks.find(x=>x.id===taskId);
  const nums=calcDisplayNums();
  const menu=document.getElementById('ctx-menu');
  document.getElementById('ctx-header').textContent=`${nums[taskId]||''} ${t.name}`;
  menu.style.display='block';
  menu.style.left=Math.min(e.clientX,window.innerWidth-220)+'px';
  menu.style.top=Math.min(e.clientY,window.innerHeight-200)+'px';
}
function closeCtxMenu(){document.getElementById('ctx-menu').style.display='none';ctxTargetId=null;}
function ctxAddSibling(){closeCtxMenu();const t=tasks.find(x=>x.id===ctxTargetId);openAddModal(t?t.parentId:null,null);}
function ctxAddChild(){closeCtxMenu();openAddModal(ctxTargetId,null);}
function ctxEdit(){closeCtxMenu();selectTask(ctxTargetId);}
function ctxDelete(){closeCtxMenu();deleteTask(ctxTargetId,null);}
document.addEventListener('click',closeCtxMenu);
document.addEventListener('keydown',e=>{if(e.key==='Escape')closeCtxMenu();});

function ganttToggleCollapse(id, e){
  e.stopPropagation();
  const scrollEl=document.getElementById('gantt-root');
  const scrollX=scrollEl?scrollEl.scrollLeft:0;
  collapsedSet.has(id)?collapsedSet.delete(id):collapsedSet.add(id);
  renderGantt();
  requestAnimationFrame(()=>{
    const el=document.getElementById('gantt-root');
    if(el)el.scrollLeft=scrollX;
  });
  saveToLS();
}

function ganttExpandAll(){
  const scrollEl=document.getElementById('gantt-root');
  const scrollX=scrollEl?scrollEl.scrollLeft:0;
  collapsedSet.clear();
  renderGantt();
  requestAnimationFrame(()=>{const el=document.getElementById('gantt-root');if(el)el.scrollLeft=scrollX;});
  saveToLS();
}

function ganttCollapseAll(){
  const scrollEl=document.getElementById('gantt-root');
  const scrollX=scrollEl?scrollEl.scrollLeft:0;
  tasks.filter(t=>hasChildren(t.id)).forEach(t=>collapsedSet.add(t.id));
  renderGantt();
  requestAnimationFrame(()=>{const el=document.getElementById('gantt-root');if(el)el.scrollLeft=scrollX;});
  saveToLS();
}

// ─── Tab switch ───
function switchTab(tab){
  currentTab=tab;
  document.getElementById('list-view').style.display=tab==='list'?'block':'none';
  document.getElementById('gantt-view').style.display=tab==='gantt'?'flex':'none';
  document.querySelectorAll('.tab-btn').forEach((b,i)=>b.classList.toggle('active',(i===0&&tab==='list')||(i===1&&tab==='gantt')));
  const lb=document.getElementById('lightning-btn');
  if(lb) lb.style.display=tab==='gantt'?'inline-flex':'none';
  const sb=document.getElementById('gantt-scale-btns');
  if(sb) sb.style.display=tab==='gantt'?'flex':'none';
  if(tab==='gantt'){
    _ganttFirstRender=true; // タブを開くたびにToday中央表示
    renderGantt();
    // アクティブスケールボタンを初期化
    document.querySelectorAll('.gantt-scale-btn').forEach(b=>{
      b.classList.toggle('active',b.dataset.scale===ganttScale);
    });
  }
}
function renderAll(){
  saveCurrentTasks();
  saveToLS();
  if(currentTab==='list')renderList();
  else renderGantt();
  updateStats();
  updateProjectUI();
}

// ─── Help Modal ───
function openHelpModal(){
  document.getElementById('help-modal').classList.add('open');
  switchHelpTab('prepare');
}
function closeHelpModal(){
  document.getElementById('help-modal').classList.remove('open');
}
function switchHelpTab(tab){
  ['prepare','basic','gantt','share','tips'].forEach(t=>{
    const body=document.getElementById('help-tab-'+t);
    const btn=document.querySelector('.help-tab[onclick*="'+t+'"]');
    if(body) body.style.display=t===tab?'block':'none';
    if(btn) btn.classList.toggle('active',t===tab);
  });
}
document.getElementById('help-modal').addEventListener('click',function(e){
  if(e.target===this) closeHelpModal();
});
function toggleSidebar(){
  sidebarCollapsed=!sidebarCollapsed;
  const sb=document.getElementById('sidebar'),btn=document.getElementById('sidebar-toggle');
  sb.classList.toggle('collapsed',sidebarCollapsed);
  btn.textContent=sidebarCollapsed?'▶':'◀';
  btn.title=sidebarCollapsed?'サイドバーを展開':'サイドバーを折りたたむ';
}

// ─── Export CSV ───
const CSV_HEADERS=['ID','No','タスク名','種別','成果物','ステータス','担当者','開始日','終了日','進捗率','依存関係（ID）','依存関係（No）','親ID','備考'];
function exportCSV(){
  const nums=calcDisplayNums();
  const rows=buildTreeOrder().map(t=>[
    t.id,                                          // 内部ID
    nums[t.id]||'',                                // 表示No
    t.name,
    t.type==='folder'?'フォルダ':'タスク',
    t.deliverable||'',
    STATUS_LABEL[t.status],
    t.assignee||'',
    t.start||'',
    t.end||'',
    t.progress+'%',
    (t.deps||[]).join(' | '),                      // 依存関係（内部ID）
    (t.deps||[]).map(d=>nums[d]||d).join(' | '),   // 依存関係（表示No）
    t.parentId||'',                                // 親ID
    t.note||''
  ]);
  const csv=[CSV_HEADERS,...rows].map(r=>r.map(v=>'"'+String(v).replace(/"/g,'""')+'"').join(',')).join('\n');
  const blob=new Blob(['\uFEFF'+csv],{type:'text/csv;charset=utf-8;'});
  const a=document.createElement('a');a.href=URL.createObjectURL(blob);a.download='wbs_export.csv';a.click();
}

// ─── Import CSV ───
function triggerImport(){document.getElementById('import-file-input').click();}
function importCSV(event){
  const file=event.target.files[0];if(!file)return;
  const reader=new FileReader();
  reader.onload=e=>{
    try{
      const text=e.target.result.replace(/^\uFEFF/,'');
      const lines=text.split(/\r?\n/).filter(l=>l.trim());
      if(!lines.length){alert('ファイルが空です');return;}

      const parseRow=line=>{
        const r=[];let c='',inQ=false;
        for(let i=0;i<line.length;i++){
          const ch=line[i];
          if(ch==='"'){if(inQ&&line[i+1]==='"'){c+='"';i++;}else inQ=!inQ;}
          else if(ch===','&&!inQ){r.push(c);c='';}
          else c+=ch;
        }
        r.push(c);return r.map(s=>s.trim());
      };

      const header=parseRow(lines[0]);
      const col=name=>header.findIndex(h=>h===name);

      // 列インデックス
      const iId   =col('ID');
      const iNo   =col('No');
      const iName =col('タスク名');
      const iType =col('種別');
      const iDel  =col('成果物');
      const iStat =col('ステータス');
      const iAsgn =col('担当者');
      const iStart=col('開始日');
      const iEnd  =col('終了日');
      const iProg =col('進捗率');
      const iDepsId=col('依存関係（ID）');   // 内部ID列
      const iDepsNo=col('依存関係（No）');   // No列（フォールバック）
      const iDepsLegacy=col('依存関係');     // 旧形式フォールバック
      const iParentId=col('親ID');
      const iNote =col('備考');

      if(iName<0){alert('CSVフォーマットが不正です。「タスク名」列が必要です。');return;}

      const hasInternalId = iId>=0;  // 内部ID列があるかどうか

      // インポートモードを選択
      let importMode='overwrite';
      if(hasInternalId && tasks.length>0){
        const choice=confirm(
          '内部ID列が検出されました。\n\n'
          +'[OK] アップサート（ID一致→更新、新規ID→追加、CSV未記載は保持）\n'
          +'[キャンセル] 上書き（現在のデータをすべて置き換え）'
        );
        importMode=choice?'upsert':'overwrite';
      } else {
        if(!confirm('インポートします。現在のデータは上書きされます。続行しますか？'))return;
      }

      const STATUS_FROM={'未着手':'todo','進行中':'doing','完了':'done','ブロック中':'block'};

      // 日付正規化（YYYY-MM-DD に統一）
      const normDate=v=>{
        if(!v) return null;
        const s=String(v).trim();
        if(!s) return null;
        if(/^\d{4}-\d{2}-\d{2}$/.test(s)) return s;
        try{
          const d=new Date(s);
          if(isNaN(d.getTime())) return null;
          return d.toISOString().slice(0,10);
        }catch(e){ return null; }
      };

      // ── パース：全行を読んでタスクオブジェクトを生成 ──
      const noToId={};   // No → 内部ID（既存または新規）
      const parsed=[];

      for(let i=1;i<lines.length;i++){
        const r=parseRow(lines[i]);
        const name=iName>=0?r[iName]:'';
        if(!name) continue;

        // 内部IDの決定
        let taskId=iId>=0?r[iId]:'';
        if(!taskId){
          // 旧形式CSVの場合：Noから既存タスクを探すか新規生成
          const no=iNo>=0?r[iNo]:'';
          const existByNo=no?tasks.find(t=>calcDisplayNums()[t.id]===no):null;
          taskId=existByNo?existByNo.id:uid();
        }

        const no=iNo>=0?r[iNo]:'';
        if(no) noToId[no]=taskId;

        const type=(iType>=0&&r[iType]==='フォルダ')?'folder':'task';
        const prog=parseInt(String(iProg>=0?r[iProg]:'0').replace('%',''))||0;
        const statusRaw=iStat>=0?r[iStat]:'';

        // 依存関係：内部ID列→No列→旧形式列の優先順
        let depsRaw='';
        if(iDepsId>=0&&r[iDepsId]) depsRaw=r[iDepsId];
        else if(iDepsNo>=0&&r[iDepsNo]) depsRaw=r[iDepsNo];
        else if(iDepsLegacy>=0&&r[iDepsLegacy]) depsRaw=r[iDepsLegacy];

        parsed.push({
          id:taskId, _no:no,
          _depsRaw:depsRaw,
          _depsAreIds:iDepsId>=0&&!!r[iDepsId], // trueなら依存はすでに内部ID
          _parentIdRaw:iParentId>=0?r[iParentId]:'',
          parentId:null,
          type, name,
          deliverable:iDel>=0?r[iDel]:'',
          status:STATUS_FROM[statusRaw]||'todo',
          assignee:iAsgn>=0?r[iAsgn]:'',
          start:normDate(iStart>=0?r[iStart]:null),
          end:normDate(iEnd>=0?r[iEnd]:null),
          progress:prog,
          deps:[],
          note:iNote>=0?r[iNote]:''
        });
      }

      // ── 第2パス：parentId・deps を解決 ──
      parsed.forEach(t=>{
        // parentId解決
        if(iParentId>=0&&t._parentIdRaw){
          // 内部ID形式（t123）かNoかを判定
          if(t._parentIdRaw.startsWith('t')){
            t.parentId=t._parentIdRaw;
          } else {
            t.parentId=noToId[t._parentIdRaw]||null;
          }
        } else if(t._no&&t._no.includes('.')){
          // NoからparentIdを推定（旧形式フォールバック）
          const parentNo=t._no.split('.').slice(0,-1).join('.');
          t.parentId=noToId[parentNo]||null;
        }

        // deps解決
        t.deps=(t._depsRaw||'').split('|').map(s=>s.trim()).filter(Boolean).map(depStr=>{
          if(!depStr) return null;
          if(t._depsAreIds) return depStr; // すでに内部ID
          // Noとして解決を試みる
          return noToId[depStr]||depStr;
        }).filter(Boolean);

        delete t._no; delete t._depsRaw; delete t._depsAreIds; delete t._parentIdRaw;
      });

      // ── インポートモード別処理 ──
      if(importMode==='upsert'){
        // アップサート：ID一致→フィールド更新、新規ID→追加
        const parsedIds=new Set(parsed.map(t=>t.id));
        parsed.forEach(incoming=>{
          const existing=tasks.find(t=>t.id===incoming.id);
          if(existing){
            // 既存タスクを更新（全フィールド上書き）
            Object.assign(existing,incoming);
          } else {
            // 新規タスクを追加
            tasks.push(incoming);
          }
        });
        // _uid カウンターを既存IDより大きい値に更新
        tasks.forEach(t=>{
          const n=parseInt((t.id||'').replace('t',''))||0;
          if(n>=_uid) _uid=n+1;
        });
        const p=currentProject();if(p)p.tasks=tasks;
        alert('✅ アップサート完了：'+parsed.length+'件を処理しました');
      } else {
        // 上書き
        tasks=parsed;
        const p=currentProject();if(p)p.tasks=parsed;
        // _uid を更新
        parsed.forEach(t=>{
          const n=parseInt((t.id||'').replace('t',''))||0;
          if(n>=_uid) _uid=n+1;
        });
        alert('✅ '+parsed.length+'件をインポートしました');
      }

      collapsedSet.clear();selectedTaskId=null;
      document.getElementById('detail-panel').classList.remove('open');
      renderAll();
    }catch(err){alert('インポートに失敗しました:\n'+err.message);}
    finally{event.target.value='';}
  };
  reader.readAsText(file,'UTF-8');
}

// ─── Init ───
let currentTab='list';
let selectedTaskId=null;
let collapsedSet=new Set();
let sidebarCollapsed=false;

// 1. ストレージメタ読み込み
loadStorageMeta();

// 2. localStorageからデータ復元
initProjects();
initUsers();

// 3. IDBからハンドル復元（非同期）→ バナー・UI更新
(async()=>{
  if(storageMode==='csvFile'){
    await tryRestoreHandleFromIDB(); // ハンドルをcsvDirHandleに復元
    updateLoginCsvBanner();          // ワンクリックボタンを表示
    updateStorageIndicator();
  }
})();

// 4. UI描画
updateProjectUI();
updateStorageIndicator();
isEditMode=storageMode==='localStorage';
updateEditModeUI();
renderAll();
startCsvPolling();
</script>
</body>
</html>
