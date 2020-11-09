---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308696"
---
# <span data-ttu-id="fdf13-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="fdf13-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="fdf13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdf13-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf13-103">구독에 대 한 리소스 간에 허용 된 트래픽을 표시 하는 데 사용 됨</span><span class="sxs-lookup"><span data-stu-id="fdf13-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="fdf13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fdf13-104">SYNTAX</span></span>

### <span data-ttu-id="fdf13-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fdf13-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdf13-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="fdf13-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdf13-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdf13-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fdf13-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fdf13-108">DESCRIPTION</span></span>
<span data-ttu-id="fdf13-109">연결 형식에 따라 구독 및 위치에 대 한 리소스 사이의 모든 가능 트래픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fdf13-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="fdf13-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fdf13-110">EXAMPLES</span></span>

### <span data-ttu-id="fdf13-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fdf13-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="fdf13-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="fdf13-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="fdf13-113">연결 형식에 따라 구독 및 위치에 대 한 리소스 사이의 모든 가능 트래픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fdf13-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="fdf13-114">변수</span><span class="sxs-lookup"><span data-stu-id="fdf13-114">PARAMETERS</span></span>

### <span data-ttu-id="fdf13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf13-115">-DefaultProfile</span></span>
<span data-ttu-id="fdf13-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf13-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdf13-117">-위치</span><span class="sxs-lookup"><span data-stu-id="fdf13-117">-Location</span></span>
<span data-ttu-id="fdf13-118">Location.</span><span class="sxs-lookup"><span data-stu-id="fdf13-118">Location.</span></span>

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

### <span data-ttu-id="fdf13-119">-이름</span><span class="sxs-lookup"><span data-stu-id="fdf13-119">-Name</span></span>
<span data-ttu-id="fdf13-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf13-120">Resource name.</span></span>

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

### <span data-ttu-id="fdf13-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf13-121">-ResourceGroupName</span></span>
<span data-ttu-id="fdf13-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf13-122">Resource group name.</span></span>

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

### <span data-ttu-id="fdf13-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdf13-123">-ResourceId</span></span>
<span data-ttu-id="fdf13-124">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf13-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="fdf13-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf13-125">CommonParameters</span></span>
<span data-ttu-id="fdf13-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf13-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf13-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf13-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf13-128">입력</span><span class="sxs-lookup"><span data-stu-id="fdf13-128">INPUTS</span></span>

### <span data-ttu-id="fdf13-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fdf13-129">System.String</span></span>

## <span data-ttu-id="fdf13-130">출력</span><span class="sxs-lookup"><span data-stu-id="fdf13-130">OUTPUTS</span></span>

### <span data-ttu-id="fdf13-131">Microsoft. Azure. AllowedConnection. PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="fdf13-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="fdf13-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fdf13-132">NOTES</span></span>

## <span data-ttu-id="fdf13-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdf13-133">RELATED LINKS</span></span>
