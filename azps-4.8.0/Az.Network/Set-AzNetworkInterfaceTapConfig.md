---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214772"
---
# <span data-ttu-id="9ea9e-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9ea9e-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="9ea9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ea9e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea9e-103">네트워크 인터페이스에 대 한 탭 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="9ea9e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ea9e-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ea9e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ea9e-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea9e-106">**AzNetworkInterfaceTapConfig** 에서 네트워크 인터페이스에 대 한 탭 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="9ea9e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9ea9e-107">EXAMPLES</span></span>

### <span data-ttu-id="9ea9e-108">예제 1: 업데이트 된 TapConfig 이름을 사용 하 여 TapConfiguration 설정</span><span class="sxs-lookup"><span data-stu-id="9ea9e-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="9ea9e-109">변수</span><span class="sxs-lookup"><span data-stu-id="9ea9e-109">PARAMETERS</span></span>

### <span data-ttu-id="9ea9e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ea9e-110">-AsJob</span></span>
<span data-ttu-id="9ea9e-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9ea9e-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ea9e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea9e-112">-DefaultProfile</span></span>
<span data-ttu-id="9ea9e-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ea9e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9ea9e-114">-Force</span></span>
<span data-ttu-id="9ea9e-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ea9e-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9ea9e-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="9ea9e-117">NetworkInterface 탭 구성</span><span class="sxs-lookup"><span data-stu-id="9ea9e-117">The NetworkInterface Tap configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ea9e-118">-확인</span><span class="sxs-lookup"><span data-stu-id="9ea9e-118">-Confirm</span></span>
<span data-ttu-id="9ea9e-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ea9e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea9e-120">-WhatIf</span></span>
<span data-ttu-id="9ea9e-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ea9e-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ea9e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea9e-123">CommonParameters</span></span>
<span data-ttu-id="9ea9e-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea9e-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ea9e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea9e-126">입력</span><span class="sxs-lookup"><span data-stu-id="9ea9e-126">INPUTS</span></span>

### <span data-ttu-id="9ea9e-127">PSNetworkInterfaceTapConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="9ea9e-128">출력</span><span class="sxs-lookup"><span data-stu-id="9ea9e-128">OUTPUTS</span></span>

### <span data-ttu-id="9ea9e-129">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="9ea9e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9ea9e-130">NOTES</span></span>

## <span data-ttu-id="9ea9e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ea9e-131">RELATED LINKS</span></span>

[<span data-ttu-id="9ea9e-132">추가-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9ea9e-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="9ea9e-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9ea9e-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="9ea9e-134">제거-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9ea9e-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
