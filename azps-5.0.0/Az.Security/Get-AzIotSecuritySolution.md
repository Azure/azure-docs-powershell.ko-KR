---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226186"
---
# <span data-ttu-id="b03ce-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b03ce-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="b03ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b03ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b03ce-103">IoT security 솔루션 다운로드</span><span class="sxs-lookup"><span data-stu-id="b03ce-103">Get IoT security solution</span></span>

## <span data-ttu-id="b03ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b03ce-104">SYNTAX</span></span>

### <span data-ttu-id="b03ce-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b03ce-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03ce-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="b03ce-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b03ce-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b03ce-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b03ce-108">리소스</span><span class="sxs-lookup"><span data-stu-id="b03ce-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b03ce-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b03ce-109">DESCRIPTION</span></span>
<span data-ttu-id="b03ce-110">Get-AzIotSecuritySolution cmdlet은 하나 이상의 iot security 솔루션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b03ce-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="b03ce-111">IoT security 솔루션은 iot 디바이스 및 iot hub의 보안 데이터 및 이벤트를 수집 하 여 위협을 방지 하 고 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b03ce-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="b03ce-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b03ce-112">EXAMPLES</span></span>

### <span data-ttu-id="b03ce-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="b03ce-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="b03ce-114">리소스 그룹 "MyResourceGroup"에서 "MySample" 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="b03ce-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="b03ce-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="b03ce-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="b03ce-116">리소스 그룹 "MyResourceGroup"의 모든 보안 솔루션 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="b03ce-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="b03ce-117">변수</span><span class="sxs-lookup"><span data-stu-id="b03ce-117">PARAMETERS</span></span>

### <span data-ttu-id="b03ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03ce-118">-DefaultProfile</span></span>
<span data-ttu-id="b03ce-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b03ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03ce-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b03ce-120">-Name</span></span>
<span data-ttu-id="b03ce-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b03ce-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="b03ce-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b03ce-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03ce-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b03ce-124">-ResourceId</span></span>
<span data-ttu-id="b03ce-125">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b03ce-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b03ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03ce-126">CommonParameters</span></span>
<span data-ttu-id="b03ce-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b03ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03ce-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b03ce-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03ce-129">입력</span><span class="sxs-lookup"><span data-stu-id="b03ce-129">INPUTS</span></span>

### <span data-ttu-id="b03ce-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b03ce-130">System.String</span></span>

## <span data-ttu-id="b03ce-131">출력</span><span class="sxs-lookup"><span data-stu-id="b03ce-131">OUTPUTS</span></span>

### <span data-ttu-id="b03ce-132">Microsoft. Azure. .Prootsecuritysecuritysolutions 솔루션.</span><span class="sxs-lookup"><span data-stu-id="b03ce-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="b03ce-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b03ce-133">NOTES</span></span>

## <span data-ttu-id="b03ce-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b03ce-134">RELATED LINKS</span></span>
