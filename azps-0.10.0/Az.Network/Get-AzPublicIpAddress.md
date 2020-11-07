---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: b9eaacb9a9d779814fc5f0b873aa8e98afedd362
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875528"
---
# <span data-ttu-id="09976-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09976-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="09976-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09976-102">SYNOPSIS</span></span>
<span data-ttu-id="09976-103">공용 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09976-103">Gets a public IP address.</span></span>

## <span data-ttu-id="09976-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09976-104">SYNTAX</span></span>

### <span data-ttu-id="09976-105">NoExpandStandAloneIp (기본값)</span><span class="sxs-lookup"><span data-stu-id="09976-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09976-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="09976-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09976-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="09976-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09976-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="09976-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09976-109">설명은</span><span class="sxs-lookup"><span data-stu-id="09976-109">DESCRIPTION</span></span>
<span data-ttu-id="09976-110">**AzPublicIPAddress** cmdlet은 리소스 그룹에 하나 이상의 공용 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09976-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="09976-111">예제의</span><span class="sxs-lookup"><span data-stu-id="09976-111">EXAMPLES</span></span>

### <span data-ttu-id="09976-112">1: 공용 IP 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="09976-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="09976-113">이 명령은 리소스 그룹 $rgName에서 이름이 $publicIPName 인 공용 IP 주소 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09976-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="09976-114">변수</span><span class="sxs-lookup"><span data-stu-id="09976-114">PARAMETERS</span></span>

### <span data-ttu-id="09976-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09976-115">-DefaultProfile</span></span>
<span data-ttu-id="09976-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09976-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09976-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="09976-117">-ExpandResource</span></span>
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

### <span data-ttu-id="09976-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="09976-118">-IpConfigurationName</span></span>
<span data-ttu-id="09976-119">네트워크 인터페이스 IP 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09976-119">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="09976-120">-이름</span><span class="sxs-lookup"><span data-stu-id="09976-120">-Name</span></span>
<span data-ttu-id="09976-121">이 cmdlet이 가져오는 공용 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09976-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="09976-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="09976-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="09976-123">가상 컴퓨터 네트워크 인터페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09976-123">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="09976-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09976-124">-ResourceGroupName</span></span>
<span data-ttu-id="09976-125">이 cmdlet이 가져오는 공용 IP 주소를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09976-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="09976-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="09976-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="09976-127">가상 머신 인덱스.</span><span class="sxs-lookup"><span data-stu-id="09976-127">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="09976-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="09976-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="09976-129">가상 컴퓨터 크기 조정 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09976-129">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="09976-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09976-130">CommonParameters</span></span>
<span data-ttu-id="09976-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09976-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09976-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09976-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09976-133">입력</span><span class="sxs-lookup"><span data-stu-id="09976-133">INPUTS</span></span>

## <span data-ttu-id="09976-134">출력</span><span class="sxs-lookup"><span data-stu-id="09976-134">OUTPUTS</span></span>

### <span data-ttu-id="09976-135">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="09976-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="09976-136">상속자</span><span class="sxs-lookup"><span data-stu-id="09976-136">NOTES</span></span>

## <span data-ttu-id="09976-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09976-137">RELATED LINKS</span></span>

[<span data-ttu-id="09976-138">새로운 AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09976-138">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="09976-139">제거-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09976-139">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="09976-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09976-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


