---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2f6c4f410c7d4f92c8dcd911e0c113f2a91b304c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711811"
---
# <span data-ttu-id="0586d-101">Get-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0586d-101">Get-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="0586d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0586d-102">SYNOPSIS</span></span>
<span data-ttu-id="0586d-103">탭 구성 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-103">Gets a Tap configuration resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0586d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0586d-104">SYNTAX</span></span>

### <span data-ttu-id="0586d-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0586d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0586d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0586d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0586d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0586d-107">DESCRIPTION</span></span>
<span data-ttu-id="0586d-108">**AzureRmNetworkInterfaceTapConfig** cmdlet은 지정 된 리소스 그룹, 네트워크 인터페이스에 대 한 Azure 탭 구성을 가져오고 리소스 그룹 및 네트워크 인터페이스에서 구성 이름 또는 탭 구성 목록을 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-108">The **Get-AzureRmNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="0586d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0586d-109">EXAMPLES</span></span>

### <span data-ttu-id="0586d-110">예제 1: 지정 된 네트워크 인터페이스에 대 한 모든 탭 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="0586d-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="0586d-111">이 명령은 지정 된 네트워크 인터페이스에 추가 된 구성을 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="0586d-112">예제 2: 지정 된 탭 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="0586d-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="0586d-113">이 명령은 주어진 네트워크 인터페이스에 추가 된 특정 탭 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-113">This command gets specific tap configuration added for the given network interface.</span></span>

## <span data-ttu-id="0586d-114">변수</span><span class="sxs-lookup"><span data-stu-id="0586d-114">PARAMETERS</span></span>

### <span data-ttu-id="0586d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0586d-115">-DefaultProfile</span></span>
<span data-ttu-id="0586d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0586d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0586d-117">-Name</span></span>
<span data-ttu-id="0586d-118">특정 탭 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-118">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0586d-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="0586d-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="0586d-120">네트워크 인터페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-120">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0586d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0586d-121">-ResourceGroupName</span></span>
<span data-ttu-id="0586d-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0586d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0586d-123">-ResourceId</span></span>
<span data-ttu-id="0586d-124">TapConfiguration 리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-124">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0586d-125">-확인</span><span class="sxs-lookup"><span data-stu-id="0586d-125">-Confirm</span></span>
<span data-ttu-id="0586d-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0586d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0586d-127">-WhatIf</span></span>
<span data-ttu-id="0586d-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0586d-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0586d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0586d-130">CommonParameters</span></span>
<span data-ttu-id="0586d-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0586d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0586d-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0586d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0586d-133">입력</span><span class="sxs-lookup"><span data-stu-id="0586d-133">INPUTS</span></span>

### <span data-ttu-id="0586d-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0586d-134">System.String</span></span>

## <span data-ttu-id="0586d-135">출력</span><span class="sxs-lookup"><span data-stu-id="0586d-135">OUTPUTS</span></span>

### <span data-ttu-id="0586d-136">PSNetworkInterfaceTapConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0586d-136">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="0586d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="0586d-137">NOTES</span></span>

## <span data-ttu-id="0586d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0586d-138">RELATED LINKS</span></span>
