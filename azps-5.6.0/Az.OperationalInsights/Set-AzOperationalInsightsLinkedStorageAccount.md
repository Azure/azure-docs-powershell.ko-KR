---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1392e77ef6497265dde8bcf0a05a86529253f539
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989725"
---
# <span data-ttu-id="4bcbb-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bcbb-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="4bcbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bcbb-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcbb-103">작업 영역의 연결된 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="4bcbb-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="4bcbb-104">구문</span><span class="sxs-lookup"><span data-stu-id="4bcbb-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bcbb-105">설명</span><span class="sxs-lookup"><span data-stu-id="4bcbb-105">DESCRIPTION</span></span>
<span data-ttu-id="4bcbb-106">작업 영역의 연결된 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="4bcbb-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="4bcbb-107">예제</span><span class="sxs-lookup"><span data-stu-id="4bcbb-107">EXAMPLES</span></span>

### <span data-ttu-id="4bcbb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4bcbb-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="4bcbb-109">작업 영역의 연결된 저장소 설정</span><span class="sxs-lookup"><span data-stu-id="4bcbb-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="4bcbb-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4bcbb-110">PARAMETERS</span></span>

### <span data-ttu-id="4bcbb-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="4bcbb-111">-DataSourceType</span></span>
<span data-ttu-id="4bcbb-112">데이터 원본 형식은 'CustomLogs', 'AzureWatson' 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bcbb-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcbb-113">-DefaultProfile</span></span>
<span data-ttu-id="4bcbb-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bcbb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcbb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4bcbb-115">-Force</span></span>
<span data-ttu-id="4bcbb-116">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bcbb-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcbb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcbb-117">-ResourceGroupName</span></span>
<span data-ttu-id="4bcbb-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bcbb-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcbb-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="4bcbb-119">-StorageAccountIds</span></span>
<span data-ttu-id="4bcbb-120">저장소 계정 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4bcbb-120">list of storage account Id.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcbb-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4bcbb-121">-WorkspaceName</span></span>
<span data-ttu-id="4bcbb-122">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bcbb-122">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcbb-123">-확인</span><span class="sxs-lookup"><span data-stu-id="4bcbb-123">-Confirm</span></span>
<span data-ttu-id="4bcbb-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bcbb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcbb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bcbb-125">-WhatIf</span></span>
<span data-ttu-id="4bcbb-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4bcbb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bcbb-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bcbb-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcbb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcbb-128">CommonParameters</span></span>
<span data-ttu-id="4bcbb-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcbb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcbb-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bcbb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcbb-131">입력</span><span class="sxs-lookup"><span data-stu-id="4bcbb-131">INPUTS</span></span>

### <span data-ttu-id="4bcbb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4bcbb-132">System.String</span></span>

## <span data-ttu-id="4bcbb-133">출력</span><span class="sxs-lookup"><span data-stu-id="4bcbb-133">OUTPUTS</span></span>

### <span data-ttu-id="4bcbb-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="4bcbb-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="4bcbb-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4bcbb-135">NOTES</span></span>

## <span data-ttu-id="4bcbb-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bcbb-136">RELATED LINKS</span></span>
