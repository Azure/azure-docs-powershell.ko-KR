---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495138"
---
# <span data-ttu-id="de481-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="de481-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="de481-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de481-102">SYNOPSIS</span></span>
<span data-ttu-id="de481-103">ExpressRoutePort에 할당된 ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="de481-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="de481-104">구문</span><span class="sxs-lookup"><span data-stu-id="de481-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de481-105">설명</span><span class="sxs-lookup"><span data-stu-id="de481-105">DESCRIPTION</span></span>
<span data-ttu-id="de481-106">**Set-AzExpressRoutePortIdentity** cmdlet은 로컬 Azure ExpressRoutePort 개체를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="de481-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="de481-107">**Set-AzExpressRoutePort를** 사용하여 ExpressRoutePort에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="de481-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="de481-108">예제</span><span class="sxs-lookup"><span data-stu-id="de481-108">EXAMPLES</span></span>

### <span data-ttu-id="de481-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="de481-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="de481-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de481-110">PARAMETERS</span></span>

### <span data-ttu-id="de481-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de481-111">-DefaultProfile</span></span>
<span data-ttu-id="de481-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de481-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de481-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="de481-113">-ExpressRoutePort</span></span>
<span data-ttu-id="de481-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="de481-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="de481-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="de481-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="de481-116">ExpressRoutePort에 할당할 사용자 할당 ID의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="de481-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="de481-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de481-117">-Confirm</span></span>
<span data-ttu-id="de481-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="de481-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de481-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de481-119">-WhatIf</span></span>
<span data-ttu-id="de481-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="de481-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de481-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="de481-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de481-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de481-122">CommonParameters</span></span>
<span data-ttu-id="de481-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="de481-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de481-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="de481-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de481-125">입력</span><span class="sxs-lookup"><span data-stu-id="de481-125">INPUTS</span></span>

### <span data-ttu-id="de481-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="de481-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="de481-127">System.String</span><span class="sxs-lookup"><span data-stu-id="de481-127">System.String</span></span>

## <span data-ttu-id="de481-128">출력</span><span class="sxs-lookup"><span data-stu-id="de481-128">OUTPUTS</span></span>

### <span data-ttu-id="de481-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="de481-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="de481-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="de481-130">NOTES</span></span>

## <span data-ttu-id="de481-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de481-131">RELATED LINKS</span></span>
[<span data-ttu-id="de481-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="de481-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="de481-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="de481-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="de481-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="de481-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
