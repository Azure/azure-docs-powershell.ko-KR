---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 1404acfa32de79096e990adbe2f66b43af0d4e96
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882922"
---
# <span data-ttu-id="0e5ae-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e5ae-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="0e5ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="0e5ae-103">공용 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e5ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e5ae-104">SYNTAX</span></span>

### <span data-ttu-id="0e5ae-105">NoExpandStandAloneIp (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e5ae-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e5ae-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="0e5ae-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e5ae-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="0e5ae-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e5ae-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="0e5ae-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e5ae-109">설명은</span><span class="sxs-lookup"><span data-stu-id="0e5ae-109">DESCRIPTION</span></span>
<span data-ttu-id="0e5ae-110">**AzureRmPublicIPAddress** cmdlet은 리소스 그룹에 하나 이상의 공용 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="0e5ae-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0e5ae-111">EXAMPLES</span></span>

### <span data-ttu-id="0e5ae-112">1: 공용 IP 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="0e5ae-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="0e5ae-113">이 명령은 리소스 그룹 $rgName에서 이름이 $publicIPName 인 공용 IP 주소 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="0e5ae-114">변수</span><span class="sxs-lookup"><span data-stu-id="0e5ae-114">PARAMETERS</span></span>

### <span data-ttu-id="0e5ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e5ae-115">-DefaultProfile</span></span>
<span data-ttu-id="0e5ae-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ae-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="0e5ae-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ae-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0e5ae-118">-IpConfigurationName</span></span>
<span data-ttu-id="0e5ae-119">네트워크 인터페이스 IP 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-119">Network Interface IP Configuration Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ae-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0e5ae-120">-Name</span></span>
<span data-ttu-id="0e5ae-121">이 cmdlet이 가져오는 공용 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ae-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="0e5ae-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="0e5ae-123">가상 컴퓨터 네트워크 인터페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-123">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e5ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e5ae-125">이 cmdlet이 가져오는 공용 IP 주소를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ae-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="0e5ae-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="0e5ae-127">가상 머신 인덱스.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-127">Virtual Machine Index.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ae-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0e5ae-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="0e5ae-129">가상 컴퓨터 크기 조정 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-129">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e5ae-130">CommonParameters</span></span>
<span data-ttu-id="0e5ae-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e5ae-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e5ae-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e5ae-133">입력</span><span class="sxs-lookup"><span data-stu-id="0e5ae-133">INPUTS</span></span>

## <span data-ttu-id="0e5ae-134">출력</span><span class="sxs-lookup"><span data-stu-id="0e5ae-134">OUTPUTS</span></span>

### <span data-ttu-id="0e5ae-135">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0e5ae-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="0e5ae-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0e5ae-136">NOTES</span></span>

## <span data-ttu-id="0e5ae-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e5ae-137">RELATED LINKS</span></span>

[<span data-ttu-id="0e5ae-138">새로운 AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e5ae-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0e5ae-139">제거-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e5ae-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0e5ae-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e5ae-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


