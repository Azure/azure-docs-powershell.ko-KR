---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370259"
---
# <span data-ttu-id="621ae-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="621ae-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="621ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="621ae-102">SYNOPSIS</span></span>
<span data-ttu-id="621ae-103">작업 영역의 연결된 서비스 선택 또는 나열</span><span class="sxs-lookup"><span data-stu-id="621ae-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="621ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="621ae-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="621ae-105">설명</span><span class="sxs-lookup"><span data-stu-id="621ae-105">DESCRIPTION</span></span>
<span data-ttu-id="621ae-106">작업 영역의 연결된 서비스, "-LinkedServiceName"이 제공되지 않은 경우 나열</span><span class="sxs-lookup"><span data-stu-id="621ae-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="621ae-107">예제</span><span class="sxs-lookup"><span data-stu-id="621ae-107">EXAMPLES</span></span>

### <span data-ttu-id="621ae-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="621ae-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="621ae-109">작업 영역의 연결된 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="621ae-109">Get linked service for workspace</span></span>

## <span data-ttu-id="621ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="621ae-110">PARAMETERS</span></span>

### <span data-ttu-id="621ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621ae-111">-DefaultProfile</span></span>
<span data-ttu-id="621ae-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="621ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="621ae-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="621ae-113">-LinkedServiceName</span></span>
<span data-ttu-id="621ae-114">연결된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="621ae-114">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="621ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="621ae-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="621ae-116">The resource group name.</span></span>

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

### <span data-ttu-id="621ae-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="621ae-117">-WorkspaceName</span></span>
<span data-ttu-id="621ae-118">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="621ae-118">The workspace name.</span></span>

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

### <span data-ttu-id="621ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621ae-119">CommonParameters</span></span>
<span data-ttu-id="621ae-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="621ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621ae-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="621ae-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621ae-122">입력</span><span class="sxs-lookup"><span data-stu-id="621ae-122">INPUTS</span></span>

### <span data-ttu-id="621ae-123">System.String</span><span class="sxs-lookup"><span data-stu-id="621ae-123">System.String</span></span>

## <span data-ttu-id="621ae-124">출력</span><span class="sxs-lookup"><span data-stu-id="621ae-124">OUTPUTS</span></span>

### <span data-ttu-id="621ae-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="621ae-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="621ae-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="621ae-126">NOTES</span></span>

## <span data-ttu-id="621ae-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="621ae-127">RELATED LINKS</span></span>
