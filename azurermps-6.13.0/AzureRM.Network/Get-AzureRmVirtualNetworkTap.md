---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: ff9ed8220cf2b30f2e652e207cb4d63db969a8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529536"
---
# <span data-ttu-id="8460f-101">Get-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8460f-101">Get-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="8460f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8460f-102">SYNOPSIS</span></span>
<span data-ttu-id="8460f-103">가상 네트워크 탭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-103">Gets a virtual network tap</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8460f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8460f-104">SYNTAX</span></span>

### <span data-ttu-id="8460f-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8460f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8460f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8460f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8460f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8460f-107">DESCRIPTION</span></span>
<span data-ttu-id="8460f-108">**AzureRmVirtualNetworkTap** Cmdlet은 azure 가상 네트워크 탭 또는 리소스 그룹의 azure 가상 네트워크 탭 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-108">The **Get-AzureRmVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="8460f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8460f-109">EXAMPLES</span></span>

### <span data-ttu-id="8460f-110">예제 1: 가상 네트워크 가져오기 탭</span><span class="sxs-lookup"><span data-stu-id="8460f-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\>Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="8460f-111">이 명령은 "ResourceGroup1"의 지정 된 "VirtualTap1"에 대 한 VirtualNetwork 탭 참조를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

## <span data-ttu-id="8460f-112">변수</span><span class="sxs-lookup"><span data-stu-id="8460f-112">PARAMETERS</span></span>

### <span data-ttu-id="8460f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8460f-113">-DefaultProfile</span></span>
<span data-ttu-id="8460f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8460f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8460f-115">-Name</span></span>
<span data-ttu-id="8460f-116">탭의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-116">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8460f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8460f-117">-ResourceGroupName</span></span>
<span data-ttu-id="8460f-118">가상 네트워크의 리소스 그룹 이름 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-118">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="8460f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8460f-119">-ResourceId</span></span>
<span data-ttu-id="8460f-120">VirtualNetworkTap 리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-120">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="8460f-121">-확인</span><span class="sxs-lookup"><span data-stu-id="8460f-121">-Confirm</span></span>
<span data-ttu-id="8460f-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8460f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8460f-123">-WhatIf</span></span>
<span data-ttu-id="8460f-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8460f-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8460f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8460f-126">CommonParameters</span></span>
<span data-ttu-id="8460f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8460f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8460f-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8460f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8460f-129">입력</span><span class="sxs-lookup"><span data-stu-id="8460f-129">INPUTS</span></span>

### <span data-ttu-id="8460f-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8460f-130">System.String</span></span>

## <span data-ttu-id="8460f-131">출력</span><span class="sxs-lookup"><span data-stu-id="8460f-131">OUTPUTS</span></span>

### <span data-ttu-id="8460f-132">PSVirtualNetworkTap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8460f-132">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="8460f-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8460f-133">NOTES</span></span>

## <span data-ttu-id="8460f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8460f-134">RELATED LINKS</span></span>
