---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214785"
---
# <span data-ttu-id="30d3d-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="30d3d-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="30d3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="30d3d-103">ExpressRoutePort에 할당 된 id를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3d-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="30d3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30d3d-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30d3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="30d3d-106">**Set-AzExpressRoutePortIdentity** cmdlet은 로컬 Azure ExpressRoutePort 개체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3d-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="30d3d-107">**Set-AzExpressRoutePort** 를 사용 하 여 ExpressRoutePort에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3d-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="30d3d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="30d3d-108">EXAMPLES</span></span>

### <span data-ttu-id="30d3d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="30d3d-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="30d3d-110">변수</span><span class="sxs-lookup"><span data-stu-id="30d3d-110">PARAMETERS</span></span>

### <span data-ttu-id="30d3d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d3d-111">-DefaultProfile</span></span>
<span data-ttu-id="30d3d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30d3d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30d3d-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30d3d-113">-ExpressRoutePort</span></span>
<span data-ttu-id="30d3d-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30d3d-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30d3d-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="30d3d-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="30d3d-116">ExpressRoutePort에 할당할 사용자 지정 id의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="30d3d-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d3d-117">-확인</span><span class="sxs-lookup"><span data-stu-id="30d3d-117">-Confirm</span></span>
<span data-ttu-id="30d3d-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d3d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d3d-119">-WhatIf</span></span>
<span data-ttu-id="30d3d-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30d3d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30d3d-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30d3d-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d3d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d3d-122">CommonParameters</span></span>
<span data-ttu-id="30d3d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d3d-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d3d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d3d-125">입력</span><span class="sxs-lookup"><span data-stu-id="30d3d-125">INPUTS</span></span>

### <span data-ttu-id="30d3d-126">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="30d3d-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="30d3d-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="30d3d-127">System.String</span></span>

## <span data-ttu-id="30d3d-128">출력</span><span class="sxs-lookup"><span data-stu-id="30d3d-128">OUTPUTS</span></span>

### <span data-ttu-id="30d3d-129">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="30d3d-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="30d3d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="30d3d-130">NOTES</span></span>

## <span data-ttu-id="30d3d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30d3d-131">RELATED LINKS</span></span>
[<span data-ttu-id="30d3d-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="30d3d-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="30d3d-133">새로운 AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="30d3d-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="30d3d-134">제거-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="30d3d-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
