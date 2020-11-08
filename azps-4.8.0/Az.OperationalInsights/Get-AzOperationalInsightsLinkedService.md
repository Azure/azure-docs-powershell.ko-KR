---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212962"
---
# <span data-ttu-id="145f4-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="145f4-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="145f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="145f4-102">SYNOPSIS</span></span>
<span data-ttu-id="145f4-103">작업 영역에 대 한 연결 된 서비스 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="145f4-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="145f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="145f4-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="145f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="145f4-105">DESCRIPTION</span></span>
<span data-ttu-id="145f4-106">"-LinkedServiceName"가 제공 되지 않은 경우 작업 영역에 대 한 연결 된 서비스 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="145f4-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="145f4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="145f4-107">EXAMPLES</span></span>

### <span data-ttu-id="145f4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="145f4-108">Example 1</span></span>
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

<span data-ttu-id="145f4-109">작업 영역에 대 한 연결 된 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="145f4-109">Get linked service for workspace</span></span>

## <span data-ttu-id="145f4-110">변수</span><span class="sxs-lookup"><span data-stu-id="145f4-110">PARAMETERS</span></span>

### <span data-ttu-id="145f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145f4-111">-DefaultProfile</span></span>
<span data-ttu-id="145f4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="145f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="145f4-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="145f4-113">-LinkedServiceName</span></span>
<span data-ttu-id="145f4-114">연결 된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="145f4-114">The linked service name.</span></span>

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

### <span data-ttu-id="145f4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="145f4-115">-ResourceGroupName</span></span>
<span data-ttu-id="145f4-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="145f4-116">The resource group name.</span></span>

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

### <span data-ttu-id="145f4-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="145f4-117">-WorkspaceName</span></span>
<span data-ttu-id="145f4-118">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="145f4-118">The workspace name.</span></span>

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

### <span data-ttu-id="145f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145f4-119">CommonParameters</span></span>
<span data-ttu-id="145f4-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="145f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145f4-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="145f4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145f4-122">입력</span><span class="sxs-lookup"><span data-stu-id="145f4-122">INPUTS</span></span>

### <span data-ttu-id="145f4-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="145f4-123">System.String</span></span>

## <span data-ttu-id="145f4-124">출력</span><span class="sxs-lookup"><span data-stu-id="145f4-124">OUTPUTS</span></span>

### <span data-ttu-id="145f4-125">OperationalInsights. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="145f4-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="145f4-126">상속자</span><span class="sxs-lookup"><span data-stu-id="145f4-126">NOTES</span></span>

## <span data-ttu-id="145f4-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="145f4-127">RELATED LINKS</span></span>
