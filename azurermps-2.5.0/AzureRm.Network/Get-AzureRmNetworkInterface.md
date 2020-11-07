---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 263293ea117f85caf32029ee0cfbf0dff2142cc3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882945"
---
# <span data-ttu-id="6146f-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6146f-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="6146f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6146f-102">SYNOPSIS</span></span>
<span data-ttu-id="6146f-103">네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6146f-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6146f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6146f-104">SYNTAX</span></span>

### <span data-ttu-id="6146f-105">NoExpandStandAloneNic (기본값)</span><span class="sxs-lookup"><span data-stu-id="6146f-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6146f-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="6146f-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6146f-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="6146f-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6146f-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="6146f-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6146f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6146f-109">DESCRIPTION</span></span>
<span data-ttu-id="6146f-110">**AzureRmNetworkInterface** cmdlet은 리소스 그룹의 azure 네트워크 인터페이스 또는 azure 네트워크 인터페이스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6146f-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="6146f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6146f-111">EXAMPLES</span></span>

### <span data-ttu-id="6146f-112">예제 1: 모든 네트워크 인터페이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="6146f-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="6146f-113">이 명령은 현재 구독에 대 한 모든 네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6146f-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="6146f-114">예제 2: 특정 프로비저닝 상태로 모든 네트워크 인터페이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="6146f-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="6146f-115">이 명령은 프로비저닝 상태가 성공 인 리소스 그룹 ResourceGroup1 이라는 모든 네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6146f-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="6146f-116">변수</span><span class="sxs-lookup"><span data-stu-id="6146f-116">PARAMETERS</span></span>

### <span data-ttu-id="6146f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6146f-117">-DefaultProfile</span></span>
<span data-ttu-id="6146f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6146f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6146f-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6146f-119">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6146f-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6146f-120">-Name</span></span>
<span data-ttu-id="6146f-121">이 cmdlet이 가져오는 네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6146f-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6146f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6146f-122">-ResourceGroupName</span></span>
<span data-ttu-id="6146f-123">이 cmdlet이 네트워크 인터페이스를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6146f-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6146f-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="6146f-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="6146f-125">이 cmdlet이 네트워크 인터페이스를 가져오는 가상 컴퓨터 크기 조정 집합의 가상 컴퓨터 인덱스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6146f-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6146f-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6146f-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="6146f-127">이 cmdlet이 네트워크 인터페이스를 가져오는 가상 컴퓨터 크기 조정 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6146f-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6146f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6146f-128">CommonParameters</span></span>
<span data-ttu-id="6146f-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6146f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6146f-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6146f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6146f-131">입력</span><span class="sxs-lookup"><span data-stu-id="6146f-131">INPUTS</span></span>

## <span data-ttu-id="6146f-132">출력</span><span class="sxs-lookup"><span data-stu-id="6146f-132">OUTPUTS</span></span>

### <span data-ttu-id="6146f-133">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6146f-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6146f-134">상속자</span><span class="sxs-lookup"><span data-stu-id="6146f-134">NOTES</span></span>

## <span data-ttu-id="6146f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6146f-135">RELATED LINKS</span></span>

[<span data-ttu-id="6146f-136">새로운 AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6146f-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="6146f-137">제거-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6146f-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="6146f-138">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6146f-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


