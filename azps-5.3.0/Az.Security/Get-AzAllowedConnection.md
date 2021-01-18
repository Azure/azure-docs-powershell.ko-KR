---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495047"
---
# <span data-ttu-id="e9f18-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="e9f18-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="e9f18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9f18-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f18-103">구독에 대한 리소스 간에 허용된 트래픽을 표시하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9f18-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="e9f18-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9f18-104">SYNTAX</span></span>

### <span data-ttu-id="e9f18-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="e9f18-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9f18-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e9f18-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9f18-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9f18-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9f18-108">설명</span><span class="sxs-lookup"><span data-stu-id="e9f18-108">DESCRIPTION</span></span>
<span data-ttu-id="e9f18-109">연결 유형에 따라 구독 및 위치에 대한 리소스 간에 가능한 모든 트래픽 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9f18-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="e9f18-110">예제</span><span class="sxs-lookup"><span data-stu-id="e9f18-110">EXAMPLES</span></span>

### <span data-ttu-id="e9f18-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9f18-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="e9f18-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e9f18-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="e9f18-113">연결 유형에 따라 구독 및 위치에 대한 리소스 간에 가능한 모든 트래픽 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9f18-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="e9f18-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9f18-114">PARAMETERS</span></span>

### <span data-ttu-id="e9f18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f18-115">-DefaultProfile</span></span>
<span data-ttu-id="e9f18-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f18-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9f18-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e9f18-117">-Location</span></span>
<span data-ttu-id="e9f18-118">위치.</span><span class="sxs-lookup"><span data-stu-id="e9f18-118">Location.</span></span>

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

### <span data-ttu-id="e9f18-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e9f18-119">-Name</span></span>
<span data-ttu-id="e9f18-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f18-120">Resource name.</span></span>

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

### <span data-ttu-id="e9f18-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f18-121">-ResourceGroupName</span></span>
<span data-ttu-id="e9f18-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f18-122">Resource group name.</span></span>

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

### <span data-ttu-id="e9f18-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9f18-123">-ResourceId</span></span>
<span data-ttu-id="e9f18-124">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f18-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e9f18-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f18-125">CommonParameters</span></span>
<span data-ttu-id="e9f18-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f18-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f18-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e9f18-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f18-128">입력</span><span class="sxs-lookup"><span data-stu-id="e9f18-128">INPUTS</span></span>

### <span data-ttu-id="e9f18-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e9f18-129">System.String</span></span>

## <span data-ttu-id="e9f18-130">출력</span><span class="sxs-lookup"><span data-stu-id="e9f18-130">OUTPUTS</span></span>

### <span data-ttu-id="e9f18-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="e9f18-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="e9f18-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9f18-132">NOTES</span></span>

## <span data-ttu-id="e9f18-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9f18-133">RELATED LINKS</span></span>
