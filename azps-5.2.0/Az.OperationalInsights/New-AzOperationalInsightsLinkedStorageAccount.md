---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351818"
---
# <span data-ttu-id="51282-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51282-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="51282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51282-102">SYNOPSIS</span></span>
<span data-ttu-id="51282-103">작업 영역의 연결된 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="51282-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="51282-104">구문</span><span class="sxs-lookup"><span data-stu-id="51282-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51282-105">설명</span><span class="sxs-lookup"><span data-stu-id="51282-105">DESCRIPTION</span></span>
<span data-ttu-id="51282-106">작업 영역의 연결된 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="51282-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="51282-107">예제</span><span class="sxs-lookup"><span data-stu-id="51282-107">EXAMPLES</span></span>

### <span data-ttu-id="51282-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="51282-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="51282-109">작업 영역용 연결된 저장소 추가</span><span class="sxs-lookup"><span data-stu-id="51282-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="51282-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51282-110">PARAMETERS</span></span>

### <span data-ttu-id="51282-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="51282-111">-DataSourceType</span></span>
<span data-ttu-id="51282-112">데이터 원본 형식은 'CustomLogs', 'AzureWatson' 중 하나해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51282-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="51282-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51282-113">-DefaultProfile</span></span>
<span data-ttu-id="51282-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51282-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51282-115">-Force</span><span class="sxs-lookup"><span data-stu-id="51282-115">-Force</span></span>
<span data-ttu-id="51282-116">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51282-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="51282-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51282-117">-ResourceGroupName</span></span>
<span data-ttu-id="51282-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51282-118">The resource group name.</span></span>

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

### <span data-ttu-id="51282-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="51282-119">-StorageAccountIds</span></span>
<span data-ttu-id="51282-120">저장소 계정 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="51282-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="51282-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="51282-121">-WorkspaceName</span></span>
<span data-ttu-id="51282-122">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51282-122">The workspace name.</span></span>

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

### <span data-ttu-id="51282-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51282-123">-Confirm</span></span>
<span data-ttu-id="51282-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="51282-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51282-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51282-125">-WhatIf</span></span>
<span data-ttu-id="51282-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="51282-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51282-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51282-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51282-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51282-128">CommonParameters</span></span>
<span data-ttu-id="51282-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51282-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51282-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51282-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51282-131">입력</span><span class="sxs-lookup"><span data-stu-id="51282-131">INPUTS</span></span>

### <span data-ttu-id="51282-132">System.String</span><span class="sxs-lookup"><span data-stu-id="51282-132">System.String</span></span>

## <span data-ttu-id="51282-133">출력</span><span class="sxs-lookup"><span data-stu-id="51282-133">OUTPUTS</span></span>

### <span data-ttu-id="51282-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="51282-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="51282-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51282-135">NOTES</span></span>

## <span data-ttu-id="51282-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51282-136">RELATED LINKS</span></span>