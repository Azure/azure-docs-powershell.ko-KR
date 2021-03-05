---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: a542b69b1f028a7fdfd3e02d02f95735bc4add9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003344"
---
# <span data-ttu-id="8385a-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8385a-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="8385a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8385a-102">SYNOPSIS</span></span>
<span data-ttu-id="8385a-103">네트워크 인터페이스에 대한 탭 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8385a-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="8385a-104">구문</span><span class="sxs-lookup"><span data-stu-id="8385a-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8385a-105">설명</span><span class="sxs-lookup"><span data-stu-id="8385a-105">DESCRIPTION</span></span>
<span data-ttu-id="8385a-106">**Set-AzNetworkInterfaceTapConfig는** 네트워크 인터페이스에 대한 탭 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8385a-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="8385a-107">예제</span><span class="sxs-lookup"><span data-stu-id="8385a-107">EXAMPLES</span></span>

### <span data-ttu-id="8385a-108">예제 1: 업데이트된 TapConfig 이름으로 TapConfiguration 설정</span><span class="sxs-lookup"><span data-stu-id="8385a-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="8385a-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8385a-109">PARAMETERS</span></span>

### <span data-ttu-id="8385a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8385a-110">-AsJob</span></span>
<span data-ttu-id="8385a-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8385a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8385a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8385a-112">-DefaultProfile</span></span>
<span data-ttu-id="8385a-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8385a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8385a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8385a-114">-Force</span></span>
<span data-ttu-id="8385a-115">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8385a-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8385a-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8385a-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="8385a-117">NetworkInterface Tap 구성</span><span class="sxs-lookup"><span data-stu-id="8385a-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="8385a-118">-확인</span><span class="sxs-lookup"><span data-stu-id="8385a-118">-Confirm</span></span>
<span data-ttu-id="8385a-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8385a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8385a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8385a-120">-WhatIf</span></span>
<span data-ttu-id="8385a-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8385a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8385a-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8385a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8385a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8385a-123">CommonParameters</span></span>
<span data-ttu-id="8385a-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8385a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8385a-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8385a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8385a-126">입력</span><span class="sxs-lookup"><span data-stu-id="8385a-126">INPUTS</span></span>

### <span data-ttu-id="8385a-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="8385a-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="8385a-128">출력</span><span class="sxs-lookup"><span data-stu-id="8385a-128">OUTPUTS</span></span>

### <span data-ttu-id="8385a-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8385a-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="8385a-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8385a-130">NOTES</span></span>

## <span data-ttu-id="8385a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8385a-131">RELATED LINKS</span></span>

[<span data-ttu-id="8385a-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8385a-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8385a-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8385a-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8385a-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8385a-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
