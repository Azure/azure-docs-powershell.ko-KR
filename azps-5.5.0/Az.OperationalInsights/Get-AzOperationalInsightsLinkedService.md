---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184113"
---
# <span data-ttu-id="85dd6-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="85dd6-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="85dd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="85dd6-103">작업 영역의 연결된 서비스 선택 또는 나열</span><span class="sxs-lookup"><span data-stu-id="85dd6-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="85dd6-104">구문</span><span class="sxs-lookup"><span data-stu-id="85dd6-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85dd6-105">설명</span><span class="sxs-lookup"><span data-stu-id="85dd6-105">DESCRIPTION</span></span>
<span data-ttu-id="85dd6-106">작업 영역의 연결된 서비스, "-LinkedServiceName"이 제공되지 않은 경우 나열</span><span class="sxs-lookup"><span data-stu-id="85dd6-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="85dd6-107">예제</span><span class="sxs-lookup"><span data-stu-id="85dd6-107">EXAMPLES</span></span>

### <span data-ttu-id="85dd6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="85dd6-108">Example 1</span></span>
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

<span data-ttu-id="85dd6-109">작업 영역의 연결된 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="85dd6-109">Get linked service for workspace</span></span>

## <span data-ttu-id="85dd6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85dd6-110">PARAMETERS</span></span>

### <span data-ttu-id="85dd6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85dd6-111">-DefaultProfile</span></span>
<span data-ttu-id="85dd6-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85dd6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85dd6-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="85dd6-113">-LinkedServiceName</span></span>
<span data-ttu-id="85dd6-114">연결된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85dd6-114">The linked service name.</span></span>

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

### <span data-ttu-id="85dd6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85dd6-115">-ResourceGroupName</span></span>
<span data-ttu-id="85dd6-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85dd6-116">The resource group name.</span></span>

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

### <span data-ttu-id="85dd6-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="85dd6-117">-WorkspaceName</span></span>
<span data-ttu-id="85dd6-118">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85dd6-118">The workspace name.</span></span>

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

### <span data-ttu-id="85dd6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85dd6-119">CommonParameters</span></span>
<span data-ttu-id="85dd6-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85dd6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85dd6-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85dd6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85dd6-122">입력</span><span class="sxs-lookup"><span data-stu-id="85dd6-122">INPUTS</span></span>

### <span data-ttu-id="85dd6-123">System.String</span><span class="sxs-lookup"><span data-stu-id="85dd6-123">System.String</span></span>

## <span data-ttu-id="85dd6-124">출력</span><span class="sxs-lookup"><span data-stu-id="85dd6-124">OUTPUTS</span></span>

### <span data-ttu-id="85dd6-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="85dd6-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="85dd6-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85dd6-126">NOTES</span></span>

## <span data-ttu-id="85dd6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85dd6-127">RELATED LINKS</span></span>
