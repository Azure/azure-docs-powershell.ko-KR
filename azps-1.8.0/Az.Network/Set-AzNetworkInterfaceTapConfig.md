---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2a860c295106755c326624a0bb37de22976d072d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699992"
---
# <span data-ttu-id="b48c5-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b48c5-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="b48c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b48c5-102">SYNOPSIS</span></span>
<span data-ttu-id="b48c5-103">네트워크 인터페이스에 대 한 탭 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b48c5-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="b48c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b48c5-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b48c5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b48c5-105">DESCRIPTION</span></span>
<span data-ttu-id="b48c5-106">**AzNetworkInterfaceTapConfig** 에서 네트워크 인터페이스에 대 한 탭 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b48c5-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="b48c5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b48c5-107">EXAMPLES</span></span>

### <span data-ttu-id="b48c5-108">예제 1: 업데이트 된 TapConfig 이름을 사용 하 여 TapConfiguration 설정</span><span class="sxs-lookup"><span data-stu-id="b48c5-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="b48c5-109">변수</span><span class="sxs-lookup"><span data-stu-id="b48c5-109">PARAMETERS</span></span>

### <span data-ttu-id="b48c5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b48c5-110">-AsJob</span></span>
<span data-ttu-id="b48c5-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b48c5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b48c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48c5-112">-DefaultProfile</span></span>
<span data-ttu-id="b48c5-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b48c5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b48c5-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b48c5-114">-Force</span></span>
<span data-ttu-id="b48c5-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b48c5-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b48c5-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b48c5-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="b48c5-117">NetworkInterface 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b48c5-117">The NetworkInterface Tap configurtion</span></span>

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

### <span data-ttu-id="b48c5-118">-확인</span><span class="sxs-lookup"><span data-stu-id="b48c5-118">-Confirm</span></span>
<span data-ttu-id="b48c5-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b48c5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b48c5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b48c5-120">-WhatIf</span></span>
<span data-ttu-id="b48c5-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b48c5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b48c5-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b48c5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b48c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48c5-123">CommonParameters</span></span>
<span data-ttu-id="b48c5-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b48c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48c5-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b48c5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48c5-126">입력</span><span class="sxs-lookup"><span data-stu-id="b48c5-126">INPUTS</span></span>

### <span data-ttu-id="b48c5-127">PSNetworkInterfaceTapConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b48c5-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="b48c5-128">출력</span><span class="sxs-lookup"><span data-stu-id="b48c5-128">OUTPUTS</span></span>

### <span data-ttu-id="b48c5-129">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b48c5-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b48c5-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b48c5-130">NOTES</span></span>

## <span data-ttu-id="b48c5-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b48c5-131">RELATED LINKS</span></span>

[<span data-ttu-id="b48c5-132">추가-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b48c5-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="b48c5-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b48c5-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="b48c5-134">제거-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b48c5-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
