---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConfiguration.md
ms.openlocfilehash: ddf28cd36e091c677a7bdbd8aeb73d3a94add47c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970672"
---
# <span data-ttu-id="6f0b0-101">Get-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f0b0-101">Get-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="6f0b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="6f0b0-103">서버 구성에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="6f0b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f0b0-104">SYNTAX</span></span>

### <span data-ttu-id="6f0b0-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="6f0b0-105">List (Default)</span></span>
```
Get-AzMariaDbConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6f0b0-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6f0b0-106">Get</span></span>
```
Get-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6f0b0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6f0b0-107">GetViaIdentity</span></span>
```
Get-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6f0b0-108">설명</span><span class="sxs-lookup"><span data-stu-id="6f0b0-108">DESCRIPTION</span></span>
<span data-ttu-id="6f0b0-109">서버 구성에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="6f0b0-110">예제</span><span class="sxs-lookup"><span data-stu-id="6f0b0-110">EXAMPLES</span></span>

### <span data-ttu-id="6f0b0-111">예제 1: MariaDB 아래에 모든 구성 나열</span><span class="sxs-lookup"><span data-stu-id="6f0b0-111">Example 1: List all configuration under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConfiguration -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMariaDB/servers/configurations
audit_log_events                         Microsoft.DBforMariaDB/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMariaDB/servers/configurations
audit_log_include_users                  Microsoft.DBforMariaDB/servers/configurations
binlog_row_image                         Microsoft.DBforMariaDB/servers/configurations
character_set_server                     Microsoft.DBforMariaDB/servers/configurations
collation_server                         Microsoft.DBforMariaDB/servers/configurations
default_regex_flags                      Microsoft.DBforMariaDB/servers/configurations
default_week_format                      Microsoft.DBforMariaDB/servers/configurations
delayed_insert_limit                     Microsoft.DBforMariaDB/servers/configurations
delayed_insert_timeout                   Microsoft.DBforMariaDB/servers/configurations
delayed_queue_size                       Microsoft.DBforMariaDB/servers/configurations
div_precision_increment                  Microsoft.DBforMariaDB/servers/configurations
event_scheduler                          Microsoft.DBforMariaDB/servers/configurations
expensive_subquery_limit                 Microsoft.DBforMariaDB/servers/configurations
explicit_defaults_for_timestamp          Microsoft.DBforMariaDB/servers/configurations
group_concat_max_len                     Microsoft.DBforMariaDB/servers/configurations
histogram_size                           Microsoft.DBforMariaDB/servers/configurations
histogram_type                           Microsoft.DBforMariaDB/servers/configurations
host_cache_size                          Microsoft.DBforMariaDB/servers/configurations
init_connect                             Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_flushing                 Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_flushing_lwm             Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_hash_index               Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_hash_index_partitions    Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_hash_index_parts         Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_max_sleep_delay          Microsoft.DBforMariaDB/servers/configurations
innodb_autoextend_increment              Microsoft.DBforMariaDB/servers/configurations
innodb_autoinc_lock_mode                 Microsoft.DBforMariaDB/servers/configurations
innodb_buffer_pool_dump_pct              Microsoft.DBforMariaDB/servers/configurations
innodb_buffer_pool_size                  Microsoft.DBforMariaDB/servers/configurations
innodb_change_buffer_max_size            Microsoft.DBforMariaDB/servers/configurations
innodb_change_buffering                  Microsoft.DBforMariaDB/servers/configurations
innodb_cmp_per_index_enabled             Microsoft.DBforMariaDB/servers/configurations
innodb_compression_failure_threshold_pct Microsoft.DBforMariaDB/servers/configurations
innodb_compression_level                 Microsoft.DBforMariaDB/servers/configurations
innodb_compression_pad_pct_max           Microsoft.DBforMariaDB/servers/configurations
innodb_concurrency_tickets               Microsoft.DBforMariaDB/servers/configurations
innodb_deadlock_detect                   Microsoft.DBforMariaDB/servers/configurations
innodb_default_row_format                Microsoft.DBforMariaDB/servers/configurations
innodb_fill_factor                       Microsoft.DBforMariaDB/servers/configurations
innodb_flush_log_at_timeout              Microsoft.DBforMariaDB/servers/configurations
innodb_ft_enable_stopword                Microsoft.DBforMariaDB/servers/configurations
innodb_ft_num_word_optimize              Microsoft.DBforMariaDB/servers/configurations
innodb_ft_result_cache_limit             Microsoft.DBforMariaDB/servers/configurations
innodb_io_capacity                       Microsoft.DBforMariaDB/servers/configurations
innodb_lock_wait_timeout                 Microsoft.DBforMariaDB/servers/configurations
innodb_log_compressed_pages              Microsoft.DBforMariaDB/servers/configurations
innodb_lru_scan_depth                    Microsoft.DBforMariaDB/servers/configurations
innodb_max_dirty_pages_pct               Microsoft.DBforMariaDB/servers/configurations
innodb_max_dirty_pages_pct_lwm           Microsoft.DBforMariaDB/servers/configurations
innodb_max_purge_lag                     Microsoft.DBforMariaDB/servers/configurations
innodb_max_purge_lag_delay               Microsoft.DBforMariaDB/servers/configurations
innodb_max_undo_log_size                 Microsoft.DBforMariaDB/servers/configurations
innodb_old_blocks_pct                    Microsoft.DBforMariaDB/servers/configurations
innodb_old_blocks_time                   Microsoft.DBforMariaDB/servers/configurations
innodb_online_alter_log_max_size         Microsoft.DBforMariaDB/servers/configurations
innodb_open_files                        Microsoft.DBforMariaDB/servers/configurations
innodb_optimize_fulltext_only            Microsoft.DBforMariaDB/servers/configurations
innodb_page_cleaners                     Microsoft.DBforMariaDB/servers/configurations
innodb_purge_batch_size                  Microsoft.DBforMariaDB/servers/configurations
innodb_purge_rseg_truncate_frequency     Microsoft.DBforMariaDB/servers/configurations
innodb_random_read_ahead                 Microsoft.DBforMariaDB/servers/configurations
innodb_read_ahead_threshold              Microsoft.DBforMariaDB/servers/configurations
innodb_read_io_threads                   Microsoft.DBforMariaDB/servers/configurations
innodb_stats_auto_recalc                 Microsoft.DBforMariaDB/servers/configurations
innodb_stats_include_delete_marked       Microsoft.DBforMariaDB/servers/configurations
innodb_stats_method                      Microsoft.DBforMariaDB/servers/configurations
innodb_stats_modified_counter            Microsoft.DBforMariaDB/servers/configurations
innodb_stats_on_metadata                 Microsoft.DBforMariaDB/servers/configurations
innodb_stats_persistent                  Microsoft.DBforMariaDB/servers/configurations
innodb_stats_persistent_sample_pages     Microsoft.DBforMariaDB/servers/configurations
innodb_stats_traditional                 Microsoft.DBforMariaDB/servers/configurations
innodb_stats_transient_sample_pages      Microsoft.DBforMariaDB/servers/configurations
innodb_status_output                     Microsoft.DBforMariaDB/servers/configurations
innodb_status_output_locks               Microsoft.DBforMariaDB/servers/configurations
innodb_strict_mode                       Microsoft.DBforMariaDB/servers/configurations
innodb_sync_array_size                   Microsoft.DBforMariaDB/servers/configurations
innodb_table_locks                       Microsoft.DBforMariaDB/servers/configurations
innodb_thread_concurrency                Microsoft.DBforMariaDB/servers/configurations
innodb_thread_sleep_delay                Microsoft.DBforMariaDB/servers/configurations
innodb_undo_log_truncate                 Microsoft.DBforMariaDB/servers/configurations
innodb_write_io_threads                  Microsoft.DBforMariaDB/servers/configurations
interactive_timeout                      Microsoft.DBforMariaDB/servers/configurations
join_buffer_size                         Microsoft.DBforMariaDB/servers/configurations
join_cache_level                         Microsoft.DBforMariaDB/servers/configurations
lock_wait_timeout                        Microsoft.DBforMariaDB/servers/configurations
log_bin_trust_function_creators          Microsoft.DBforMariaDB/servers/configurations
log_output                               Microsoft.DBforMariaDB/servers/configurations
log_queries_not_using_indexes            Microsoft.DBforMariaDB/servers/configurations
log_slow_admin_statements                Microsoft.DBforMariaDB/servers/configurations
log_slow_filter                          Microsoft.DBforMariaDB/servers/configurations
log_slow_rate_limit                      Microsoft.DBforMariaDB/servers/configurations
log_slow_verbosity                       Microsoft.DBforMariaDB/servers/configurations
long_query_time                          Microsoft.DBforMariaDB/servers/configurations
low_priority_updates                     Microsoft.DBforMariaDB/servers/configurations
lower_case_table_names                   Microsoft.DBforMariaDB/servers/configurations
max_allowed_packet                       Microsoft.DBforMariaDB/servers/configurations
max_connect_errors                       Microsoft.DBforMariaDB/servers/configurations
max_connections                          Microsoft.DBforMariaDB/servers/configurations
max_delayed_threads                      Microsoft.DBforMariaDB/servers/configurations
max_digest_length                        Microsoft.DBforMariaDB/servers/configurations
max_error_count                          Microsoft.DBforMariaDB/servers/configurations
max_heap_table_size                      Microsoft.DBforMariaDB/servers/configurations
max_join_size                            Microsoft.DBforMariaDB/servers/configurations
max_length_for_sort_data                 Microsoft.DBforMariaDB/servers/configurations
max_prepared_stmt_count                  Microsoft.DBforMariaDB/servers/configurations
max_recursive_iterations                 Microsoft.DBforMariaDB/servers/configurations
max_seeks_for_key                        Microsoft.DBforMariaDB/servers/configurations
max_session_mem_used                     Microsoft.DBforMariaDB/servers/configurations
max_sort_length                          Microsoft.DBforMariaDB/servers/configurations
max_sp_recursion_depth                   Microsoft.DBforMariaDB/servers/configurations
max_user_connections                     Microsoft.DBforMariaDB/servers/configurations
max_write_lock_count                     Microsoft.DBforMariaDB/servers/configurations
min_examined_row_limit                   Microsoft.DBforMariaDB/servers/configurations
net_read_timeout                         Microsoft.DBforMariaDB/servers/configurations
net_retry_count                          Microsoft.DBforMariaDB/servers/configurations
net_write_timeout                        Microsoft.DBforMariaDB/servers/configurations
optimizer_search_depth                   Microsoft.DBforMariaDB/servers/configurations
optimizer_selectivity_sampling_limit     Microsoft.DBforMariaDB/servers/configurations
optimizer_use_condition_selectivity      Microsoft.DBforMariaDB/servers/configurations
preload_buffer_size                      Microsoft.DBforMariaDB/servers/configurations
query_store_capture_interval             Microsoft.DBforMariaDB/servers/configurations
query_store_capture_mode                 Microsoft.DBforMariaDB/servers/configurations
query_store_capture_utility_queries      Microsoft.DBforMariaDB/servers/configurations
query_store_retention_period_in_days     Microsoft.DBforMariaDB/servers/configurations
query_store_wait_sampling_capture_mode   Microsoft.DBforMariaDB/servers/configurations
query_store_wait_sampling_frequency      Microsoft.DBforMariaDB/servers/configurations
read_only                                Microsoft.DBforMariaDB/servers/configurations
server_id                                Microsoft.DBforMariaDB/servers/configurations
session_track_schema                     Microsoft.DBforMariaDB/servers/configurations
session_track_state_change               Microsoft.DBforMariaDB/servers/configurations
session_track_transaction_info           Microsoft.DBforMariaDB/servers/configurations
skip_show_database                       Microsoft.DBforMariaDB/servers/configurations
slave_parallel_threads                   Microsoft.DBforMariaDB/servers/configurations
slow_query_log                           Microsoft.DBforMariaDB/servers/configurations
sort_buffer_size                         Microsoft.DBforMariaDB/servers/configurations
sql_mode                                 Microsoft.DBforMariaDB/servers/configurations
standard_compliant_cte                   Microsoft.DBforMariaDB/servers/configurations
stored_program_cache                     Microsoft.DBforMariaDB/servers/configurations
sync_master_info                         Microsoft.DBforMariaDB/servers/configurations
sync_relay_log_info                      Microsoft.DBforMariaDB/servers/configurations
table_definition_cache                   Microsoft.DBforMariaDB/servers/configurations
table_open_cache                         Microsoft.DBforMariaDB/servers/configurations
thread_pool_max_threads                  Microsoft.DBforMariaDB/servers/configurations
thread_pool_min_threads                  Microsoft.DBforMariaDB/servers/configurations
thread_pool_prio_kickup_timer            Microsoft.DBforMariaDB/servers/configurations
thread_pool_priority                     Microsoft.DBforMariaDB/servers/configurations
thread_pool_stall_limit                  Microsoft.DBforMariaDB/servers/configurations
time_zone                                Microsoft.DBforMariaDB/servers/configurations
tx_isolation                             Microsoft.DBforMariaDB/servers/configurations
updatable_views_with_limit               Microsoft.DBforMariaDB/servers/configurations
use_stat_tables                          Microsoft.DBforMariaDB/servers/configurations
userstat                                 Microsoft.DBforMariaDB/servers/configurations
wait_timeout                             Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="6f0b0-112">이 명령은 MariaDB 아래에 있는 모든 구성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-112">This command lists all configuration under a MariaDB.</span></span>

### <span data-ttu-id="6f0b0-113">예제 2: MariaDB의 구성을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-113">Example 2: Get a configuration of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConfiguration -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Name max_connections

Name            Type
----            ----
max_connections Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="6f0b0-114">이 명령은 MariaDB의 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-114">This command gets a configuration of MariaDB.</span></span>

## <span data-ttu-id="6f0b0-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6f0b0-115">PARAMETERS</span></span>

### <span data-ttu-id="6f0b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f0b0-116">-DefaultProfile</span></span>
<span data-ttu-id="6f0b0-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f0b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f0b0-118">-InputObject</span></span>
<span data-ttu-id="6f0b0-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f0b0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6f0b0-120">-Name</span></span>
<span data-ttu-id="6f0b0-121">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f0b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f0b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f0b0-123">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6f0b0-124">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f0b0-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6f0b0-125">-ServerName</span></span>
<span data-ttu-id="6f0b0-126">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f0b0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f0b0-127">-SubscriptionId</span></span>
<span data-ttu-id="6f0b0-128">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-128">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f0b0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f0b0-129">CommonParameters</span></span>
<span data-ttu-id="6f0b0-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f0b0-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f0b0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f0b0-132">입력</span><span class="sxs-lookup"><span data-stu-id="6f0b0-132">INPUTS</span></span>

### <span data-ttu-id="6f0b0-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="6f0b0-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="6f0b0-134">출력</span><span class="sxs-lookup"><span data-stu-id="6f0b0-134">OUTPUTS</span></span>

### <span data-ttu-id="6f0b0-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f0b0-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="6f0b0-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f0b0-136">NOTES</span></span>

<span data-ttu-id="6f0b0-137">별칭</span><span class="sxs-lookup"><span data-stu-id="6f0b0-137">ALIASES</span></span>

<span data-ttu-id="6f0b0-138">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="6f0b0-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6f0b0-139">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6f0b0-140">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6f0b0-141">INPUTOBJECT <IMariaDbIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6f0b0-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6f0b0-142">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6f0b0-143">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6f0b0-144">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6f0b0-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="6f0b0-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6f0b0-146">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6f0b0-147">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6f0b0-148">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6f0b0-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6f0b0-150">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6f0b0-151">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="6f0b0-152">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6f0b0-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f0b0-153">RELATED LINKS</span></span>

