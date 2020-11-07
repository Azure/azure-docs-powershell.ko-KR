---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: df769ff4a6e4eb47bc47b881ac8c06de1fdb9e4c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875565"
---
# <span data-ttu-id="36cb8-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="36cb8-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="36cb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="36cb8-103">네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36cb8-103">Gets a network interface.</span></span>

## <span data-ttu-id="36cb8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36cb8-104">SYNTAX</span></span>

### <span data-ttu-id="36cb8-105">NoExpandStandAloneNic (기본값)</span><span class="sxs-lookup"><span data-stu-id="36cb8-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36cb8-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="36cb8-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36cb8-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="36cb8-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36cb8-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="36cb8-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36cb8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="36cb8-109">DESCRIPTION</span></span>
<span data-ttu-id="36cb8-110">**AzNetworkInterface** cmdlet은 리소스 그룹의 azure 네트워크 인터페이스 또는 azure 네트워크 인터페이스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36cb8-110">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="36cb8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="36cb8-111">EXAMPLES</span></span>

### <span data-ttu-id="36cb8-112">예제 1: 모든 네트워크 인터페이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="36cb8-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzNetworkInterface
```

<span data-ttu-id="36cb8-113">이 명령은 현재 구독에 대 한 모든 네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36cb8-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="36cb8-114">예제 2: 특정 프로비저닝 상태로 모든 네트워크 인터페이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="36cb8-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="36cb8-115">이 명령은 프로비저닝 상태가 성공 인 리소스 그룹 ResourceGroup1 이라는 모든 네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36cb8-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="36cb8-116">변수</span><span class="sxs-lookup"><span data-stu-id="36cb8-116">PARAMETERS</span></span>

### <span data-ttu-id="36cb8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36cb8-117">-DefaultProfile</span></span>
<span data-ttu-id="36cb8-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36cb8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36cb8-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="36cb8-119">-ExpandResource</span></span>
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

### <span data-ttu-id="36cb8-120">-이름</span><span class="sxs-lookup"><span data-stu-id="36cb8-120">-Name</span></span>
<span data-ttu-id="36cb8-121">이 cmdlet이 가져오는 네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36cb8-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

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

### <span data-ttu-id="36cb8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36cb8-122">-ResourceGroupName</span></span>
<span data-ttu-id="36cb8-123">이 cmdlet이 네트워크 인터페이스를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36cb8-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="36cb8-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="36cb8-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="36cb8-125">이 cmdlet이 네트워크 인터페이스를 가져오는 가상 컴퓨터 크기 조정 집합의 가상 컴퓨터 인덱스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36cb8-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="36cb8-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="36cb8-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="36cb8-127">이 cmdlet이 네트워크 인터페이스를 가져오는 가상 컴퓨터 크기 조정 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36cb8-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="36cb8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cb8-128">CommonParameters</span></span>
<span data-ttu-id="36cb8-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36cb8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cb8-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36cb8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cb8-131">입력</span><span class="sxs-lookup"><span data-stu-id="36cb8-131">INPUTS</span></span>

## <span data-ttu-id="36cb8-132">출력</span><span class="sxs-lookup"><span data-stu-id="36cb8-132">OUTPUTS</span></span>

### <span data-ttu-id="36cb8-133">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="36cb8-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="36cb8-134">상속자</span><span class="sxs-lookup"><span data-stu-id="36cb8-134">NOTES</span></span>

## <span data-ttu-id="36cb8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36cb8-135">RELATED LINKS</span></span>

[<span data-ttu-id="36cb8-136">새로운 AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="36cb8-136">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="36cb8-137">제거-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="36cb8-137">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="36cb8-138">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="36cb8-138">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


