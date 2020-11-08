---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216880"
---
# <span data-ttu-id="ee777-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee777-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="ee777-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee777-102">SYNOPSIS</span></span>
<span data-ttu-id="ee777-103">작업 영역에 대 한 연결 된 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="ee777-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="ee777-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee777-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee777-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ee777-105">DESCRIPTION</span></span>
<span data-ttu-id="ee777-106">작업 영역에 대 한 연결 된 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="ee777-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="ee777-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ee777-107">EXAMPLES</span></span>

### <span data-ttu-id="ee777-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee777-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="ee777-109">작업 영역에 연결 된 저장소 설정</span><span class="sxs-lookup"><span data-stu-id="ee777-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="ee777-110">변수</span><span class="sxs-lookup"><span data-stu-id="ee777-110">PARAMETERS</span></span>

### <span data-ttu-id="ee777-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="ee777-111">-DataSourceType</span></span>
<span data-ttu-id="ee777-112">데이터 원본 유형은 ' CustomLogs ', ' AzureWatson ' 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee777-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="ee777-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee777-113">-DefaultProfile</span></span>
<span data-ttu-id="ee777-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee777-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee777-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ee777-115">-Force</span></span>
<span data-ttu-id="ee777-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee777-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ee777-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee777-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee777-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee777-118">The resource group name.</span></span>

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

### <span data-ttu-id="ee777-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="ee777-119">-StorageAccountIds</span></span>
<span data-ttu-id="ee777-120">저장소 계정 Id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ee777-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="ee777-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ee777-121">-WorkspaceName</span></span>
<span data-ttu-id="ee777-122">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee777-122">The workspace name.</span></span>

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

### <span data-ttu-id="ee777-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ee777-123">-Confirm</span></span>
<span data-ttu-id="ee777-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee777-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee777-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee777-125">-WhatIf</span></span>
<span data-ttu-id="ee777-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee777-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee777-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee777-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee777-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee777-128">CommonParameters</span></span>
<span data-ttu-id="ee777-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee777-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee777-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ee777-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee777-131">입력</span><span class="sxs-lookup"><span data-stu-id="ee777-131">INPUTS</span></span>

### <span data-ttu-id="ee777-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee777-132">System.String</span></span>

## <span data-ttu-id="ee777-133">출력</span><span class="sxs-lookup"><span data-stu-id="ee777-133">OUTPUTS</span></span>

### <span data-ttu-id="ee777-134">OperationalInsights. PSLinkedStorageAccountsResource/.</span><span class="sxs-lookup"><span data-stu-id="ee777-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="ee777-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ee777-135">NOTES</span></span>

## <span data-ttu-id="ee777-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee777-136">RELATED LINKS</span></span>
