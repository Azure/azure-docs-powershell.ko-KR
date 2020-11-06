---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: b2034f27cb6c5332b190e3412963dde99f4c9ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524352"
---
# <span data-ttu-id="482ba-101">Set-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="482ba-101">Set-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="482ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="482ba-102">SYNOPSIS</span></span>
<span data-ttu-id="482ba-103">탭 구성의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-103">Sets the goal state of a Tap Configuration</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="482ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="482ba-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="482ba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="482ba-105">DESCRIPTION</span></span>
<span data-ttu-id="482ba-106">**AzureRmNetworkInterfaceTapConfig** 는 Azure 네트워크 인터페이스에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-106">The **Set-AzureRmNetworkInterfaceTapConfig** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="482ba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="482ba-107">EXAMPLES</span></span>

### <span data-ttu-id="482ba-108">예제 1: 업데이트 된 TapConfig 이름을 사용 하 여 TapConfiguration 설정</span><span class="sxs-lookup"><span data-stu-id="482ba-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="482ba-109">변수</span><span class="sxs-lookup"><span data-stu-id="482ba-109">PARAMETERS</span></span>

### <span data-ttu-id="482ba-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="482ba-110">-AsJob</span></span>
<span data-ttu-id="482ba-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="482ba-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="482ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482ba-112">-DefaultProfile</span></span>
<span data-ttu-id="482ba-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482ba-114">-Force</span><span class="sxs-lookup"><span data-stu-id="482ba-114">-Force</span></span>
<span data-ttu-id="482ba-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="482ba-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="482ba-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="482ba-117">NetworkInterface 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-117">The NetworkInterface Tap configurtion</span></span>

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

### <span data-ttu-id="482ba-118">-확인</span><span class="sxs-lookup"><span data-stu-id="482ba-118">-Confirm</span></span>
<span data-ttu-id="482ba-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="482ba-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="482ba-120">-WhatIf</span></span>
<span data-ttu-id="482ba-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="482ba-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="482ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482ba-123">CommonParameters</span></span>
<span data-ttu-id="482ba-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482ba-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="482ba-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482ba-126">입력</span><span class="sxs-lookup"><span data-stu-id="482ba-126">INPUTS</span></span>

### <span data-ttu-id="482ba-127">PSNetworkInterfaceTapConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="482ba-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="482ba-128">출력</span><span class="sxs-lookup"><span data-stu-id="482ba-128">OUTPUTS</span></span>

### <span data-ttu-id="482ba-129">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="482ba-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="482ba-130">상속자</span><span class="sxs-lookup"><span data-stu-id="482ba-130">NOTES</span></span>

## <span data-ttu-id="482ba-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="482ba-131">RELATED LINKS</span></span>
