---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ae174f31cdbe23a28dd9a21b44b640239e78fdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976496"
---
# <span data-ttu-id="7bb7a-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7bb7a-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="7bb7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bb7a-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb7a-103">연결된 저장소 계정 얻거나 나열</span><span class="sxs-lookup"><span data-stu-id="7bb7a-103">Get or list linked storage account</span></span>

## <span data-ttu-id="7bb7a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7bb7a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bb7a-105">설명</span><span class="sxs-lookup"><span data-stu-id="7bb7a-105">DESCRIPTION</span></span>
<span data-ttu-id="7bb7a-106">연결된 저장소 계정, "-DataSourceType"이 지정되지 않은 경우 연결된 모든 저장소 계정을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb7a-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="7bb7a-107">예제</span><span class="sxs-lookup"><span data-stu-id="7bb7a-107">EXAMPLES</span></span>

### <span data-ttu-id="7bb7a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7bb7a-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="7bb7a-109">작업 영역 {workspace-name}에 연결된 저장소 accoount 나열</span><span class="sxs-lookup"><span data-stu-id="7bb7a-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="7bb7a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7bb7a-110">PARAMETERS</span></span>

### <span data-ttu-id="7bb7a-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="7bb7a-111">-DataSourceType</span></span>
<span data-ttu-id="7bb7a-112">데이터 원본 형식은 'CustomLogs', 'AzureWatson' 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb7a-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="7bb7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb7a-113">-DefaultProfile</span></span>
<span data-ttu-id="7bb7a-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7bb7a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bb7a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bb7a-115">-ResourceGroupName</span></span>
<span data-ttu-id="7bb7a-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7bb7a-116">The resource group name.</span></span>

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

### <span data-ttu-id="7bb7a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7bb7a-117">-WorkspaceName</span></span>
<span data-ttu-id="7bb7a-118">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7bb7a-118">The workspace name.</span></span>

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

### <span data-ttu-id="7bb7a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb7a-119">CommonParameters</span></span>
<span data-ttu-id="7bb7a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb7a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb7a-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bb7a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb7a-122">입력</span><span class="sxs-lookup"><span data-stu-id="7bb7a-122">INPUTS</span></span>

### <span data-ttu-id="7bb7a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7bb7a-123">System.String</span></span>

## <span data-ttu-id="7bb7a-124">출력</span><span class="sxs-lookup"><span data-stu-id="7bb7a-124">OUTPUTS</span></span>

### <span data-ttu-id="7bb7a-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="7bb7a-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="7bb7a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7bb7a-126">NOTES</span></span>

## <span data-ttu-id="7bb7a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7bb7a-127">RELATED LINKS</span></span>