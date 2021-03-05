---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 71a715386a4d5646f1c9015244ad8a096313bb64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965600"
---
# <span data-ttu-id="c02cc-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="c02cc-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="c02cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c02cc-102">SYNOPSIS</span></span>
<span data-ttu-id="c02cc-103">작업 영역의 연결된 서비스 또는 나열</span><span class="sxs-lookup"><span data-stu-id="c02cc-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="c02cc-104">구문</span><span class="sxs-lookup"><span data-stu-id="c02cc-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c02cc-105">설명</span><span class="sxs-lookup"><span data-stu-id="c02cc-105">DESCRIPTION</span></span>
<span data-ttu-id="c02cc-106">작업 영역의 연결된 서비스, "-LinkedServiceName"이 제공되지 않은 경우 나열</span><span class="sxs-lookup"><span data-stu-id="c02cc-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="c02cc-107">예제</span><span class="sxs-lookup"><span data-stu-id="c02cc-107">EXAMPLES</span></span>

### <span data-ttu-id="c02cc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c02cc-108">Example 1</span></span>
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

<span data-ttu-id="c02cc-109">작업 영역의 연결된 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="c02cc-109">Get linked service for workspace</span></span>

## <span data-ttu-id="c02cc-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c02cc-110">PARAMETERS</span></span>

### <span data-ttu-id="c02cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02cc-111">-DefaultProfile</span></span>
<span data-ttu-id="c02cc-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c02cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c02cc-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="c02cc-113">-LinkedServiceName</span></span>
<span data-ttu-id="c02cc-114">연결된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c02cc-114">The linked service name.</span></span>

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

### <span data-ttu-id="c02cc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c02cc-115">-ResourceGroupName</span></span>
<span data-ttu-id="c02cc-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c02cc-116">The resource group name.</span></span>

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

### <span data-ttu-id="c02cc-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c02cc-117">-WorkspaceName</span></span>
<span data-ttu-id="c02cc-118">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c02cc-118">The workspace name.</span></span>

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

### <span data-ttu-id="c02cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02cc-119">CommonParameters</span></span>
<span data-ttu-id="c02cc-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c02cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02cc-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c02cc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02cc-122">입력</span><span class="sxs-lookup"><span data-stu-id="c02cc-122">INPUTS</span></span>

### <span data-ttu-id="c02cc-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c02cc-123">System.String</span></span>

## <span data-ttu-id="c02cc-124">출력</span><span class="sxs-lookup"><span data-stu-id="c02cc-124">OUTPUTS</span></span>

### <span data-ttu-id="c02cc-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="c02cc-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="c02cc-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c02cc-126">NOTES</span></span>

## <span data-ttu-id="c02cc-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c02cc-127">RELATED LINKS</span></span>
