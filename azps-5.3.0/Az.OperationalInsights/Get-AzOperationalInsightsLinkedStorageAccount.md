---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496376"
---
# <span data-ttu-id="d88a1-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d88a1-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="d88a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d88a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d88a1-103">연결된 저장소 계정 얻거나 나열</span><span class="sxs-lookup"><span data-stu-id="d88a1-103">Get or list linked storage account</span></span>

## <span data-ttu-id="d88a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="d88a1-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d88a1-105">설명</span><span class="sxs-lookup"><span data-stu-id="d88a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d88a1-106">연결된 저장소 계정을 얻습니다. "-DataSourceType"이 지정되지 않은 경우 모든 연결된 저장소 계정을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d88a1-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="d88a1-107">예제</span><span class="sxs-lookup"><span data-stu-id="d88a1-107">EXAMPLES</span></span>

### <span data-ttu-id="d88a1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d88a1-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="d88a1-109">작업 영역 {workspace-name}에 대한 연결된 저장소 계정 나열</span><span class="sxs-lookup"><span data-stu-id="d88a1-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="d88a1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d88a1-110">PARAMETERS</span></span>

### <span data-ttu-id="d88a1-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="d88a1-111">-DataSourceType</span></span>
<span data-ttu-id="d88a1-112">데이터 원본 형식은 'CustomLogs', 'AzureWatson' 중 하나해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d88a1-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d88a1-113">-DefaultProfile</span></span>
<span data-ttu-id="d88a1-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d88a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d88a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d88a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="d88a1-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d88a1-116">The resource group name.</span></span>

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

### <span data-ttu-id="d88a1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d88a1-117">-WorkspaceName</span></span>
<span data-ttu-id="d88a1-118">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d88a1-118">The workspace name.</span></span>

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

### <span data-ttu-id="d88a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88a1-119">CommonParameters</span></span>
<span data-ttu-id="d88a1-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d88a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88a1-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d88a1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88a1-122">입력</span><span class="sxs-lookup"><span data-stu-id="d88a1-122">INPUTS</span></span>

### <span data-ttu-id="d88a1-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d88a1-123">System.String</span></span>

## <span data-ttu-id="d88a1-124">출력</span><span class="sxs-lookup"><span data-stu-id="d88a1-124">OUTPUTS</span></span>

### <span data-ttu-id="d88a1-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="d88a1-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="d88a1-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d88a1-126">NOTES</span></span>

## <span data-ttu-id="d88a1-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d88a1-127">RELATED LINKS</span></span>