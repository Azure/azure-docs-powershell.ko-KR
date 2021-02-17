---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178609"
---
# <span data-ttu-id="495a2-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="495a2-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="495a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="495a2-102">SYNOPSIS</span></span>
<span data-ttu-id="495a2-103">구독에 대한 리소스 간에 허용되는 트래픽을 표시하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="495a2-104">구문</span><span class="sxs-lookup"><span data-stu-id="495a2-104">SYNTAX</span></span>

### <span data-ttu-id="495a2-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="495a2-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="495a2-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="495a2-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="495a2-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="495a2-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="495a2-108">설명</span><span class="sxs-lookup"><span data-stu-id="495a2-108">DESCRIPTION</span></span>
<span data-ttu-id="495a2-109">연결 유형에 따라 구독 및 위치에 대한 리소스 간에 가능한 모든 트래픽 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="495a2-110">예제</span><span class="sxs-lookup"><span data-stu-id="495a2-110">EXAMPLES</span></span>

### <span data-ttu-id="495a2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="495a2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="495a2-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="495a2-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="495a2-113">연결 유형에 따라 구독 및 위치에 대한 리소스 간에 가능한 모든 트래픽 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="495a2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="495a2-114">PARAMETERS</span></span>

### <span data-ttu-id="495a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495a2-115">-DefaultProfile</span></span>
<span data-ttu-id="495a2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495a2-117">-Location</span><span class="sxs-lookup"><span data-stu-id="495a2-117">-Location</span></span>
<span data-ttu-id="495a2-118">위치.</span><span class="sxs-lookup"><span data-stu-id="495a2-118">Location.</span></span>

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

### <span data-ttu-id="495a2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="495a2-119">-Name</span></span>
<span data-ttu-id="495a2-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-120">Resource name.</span></span>

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

### <span data-ttu-id="495a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="495a2-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-122">Resource group name.</span></span>

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

### <span data-ttu-id="495a2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="495a2-123">-ResourceId</span></span>
<span data-ttu-id="495a2-124">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="495a2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495a2-125">CommonParameters</span></span>
<span data-ttu-id="495a2-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495a2-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="495a2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495a2-128">입력</span><span class="sxs-lookup"><span data-stu-id="495a2-128">INPUTS</span></span>

### <span data-ttu-id="495a2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="495a2-129">System.String</span></span>

## <span data-ttu-id="495a2-130">출력</span><span class="sxs-lookup"><span data-stu-id="495a2-130">OUTPUTS</span></span>

### <span data-ttu-id="495a2-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="495a2-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="495a2-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="495a2-132">NOTES</span></span>

## <span data-ttu-id="495a2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="495a2-133">RELATED LINKS</span></span>
