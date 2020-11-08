---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046353"
---
# <span data-ttu-id="e5a96-101">Get-AzureEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5a96-101">Get-AzureEffectiveRouteTable</span></span>

## <span data-ttu-id="e5a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5a96-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a96-103">가상 컴퓨터에 적용 된 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-103">Gets the route applied in a virtual machine.</span></span>

## <span data-ttu-id="e5a96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5a96-104">SYNTAX</span></span>

### <span data-ttu-id="e5a96-105">IaaSGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="e5a96-105">IaaSGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e5a96-106">SlotGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="e5a96-106">SlotGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e5a96-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e5a96-107">DESCRIPTION</span></span>
<span data-ttu-id="e5a96-108">**AzureEffectiveRouteTable** cmdlet은 가상 컴퓨터에 적용 된 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-108">The **Get-AzureEffectiveRouteTable** cmdlet gets the route applied in a virtual machine.</span></span>
<span data-ttu-id="e5a96-109">이 작업을 완료 하는 데 몇 초 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-109">This operation could take several seconds to finish.</span></span>

## <span data-ttu-id="e5a96-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e5a96-110">EXAMPLES</span></span>

### <span data-ttu-id="e5a96-111">예제 1: 가상 컴퓨터를 적용 한 유효한 경로 가져오기</span><span class="sxs-lookup"><span data-stu-id="e5a96-111">Example 1: Get the effective route applied a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

<span data-ttu-id="e5a96-112">이 명령은 ContosoService 이라는 서비스에 대 한 ContosoVM06 이라는 가상 컴퓨터를 가져오고 현재 cmdlet에 해당 가상 컴퓨터 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="e5a96-113">현재 cmdlet은 해당 가상 컴퓨터에 적용 된 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-113">The current cmdlet gets the route applied to that virtual machine.</span></span>

## <span data-ttu-id="e5a96-114">변수</span><span class="sxs-lookup"><span data-stu-id="e5a96-114">PARAMETERS</span></span>

### <span data-ttu-id="e5a96-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="e5a96-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="e5a96-116">이 cmdlet이 유효한 경로를 가져오는 네트워크 어댑터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-116">Specifies the name of the network adapter for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a96-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="e5a96-117">-Profile</span></span>
<span data-ttu-id="e5a96-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e5a96-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a96-120">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="e5a96-120">-RoleInstanceName</span></span>
<span data-ttu-id="e5a96-121">이 cmdlet이 유효한 경로를 가져오는 PaaS 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-121">Specifies the name of a PaaS role for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a96-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e5a96-122">-ServiceName</span></span>
<span data-ttu-id="e5a96-123">클라우드 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-123">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="e5a96-124">이 cmdlet이 유효한 경로를 가져오는 PaaS 역할은이 매개 변수에서 지정 하는 서비스에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-124">The PaaS role for which this cmdlet gets effective routes belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a96-125">-슬롯</span><span class="sxs-lookup"><span data-stu-id="e5a96-125">-Slot</span></span>
<span data-ttu-id="e5a96-126">PaaS 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-126">Specifies a PaaS slot.</span></span>
<span data-ttu-id="e5a96-127">이 cmdlet이 유효한 경로를 가져오는 PaaS 역할에는이 매개 변수에서 지정 하는 슬롯이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-127">The PaaS role for which this cmdlet gets effective routes has the slot that this parameter specifies.</span></span>
<span data-ttu-id="e5a96-128">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-128">Valid values are:</span></span> 

- <span data-ttu-id="e5a96-129">프로덕션용</span><span class="sxs-lookup"><span data-stu-id="e5a96-129">Production</span></span>
- <span data-ttu-id="e5a96-130">대기</span><span class="sxs-lookup"><span data-stu-id="e5a96-130">Staging</span></span> 

<span data-ttu-id="e5a96-131">기본값은 실제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-131">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a96-132">-VM</span><span class="sxs-lookup"><span data-stu-id="e5a96-132">-VM</span></span>
<span data-ttu-id="e5a96-133">이 cmdlet이 유효한 경로를 가져오는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-133">Specifies the virtual machine object for which this cmdlet gets effective routes.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a96-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a96-134">CommonParameters</span></span>
<span data-ttu-id="e5a96-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a96-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5a96-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a96-137">입력</span><span class="sxs-lookup"><span data-stu-id="e5a96-137">INPUTS</span></span>

## <span data-ttu-id="e5a96-138">출력</span><span class="sxs-lookup"><span data-stu-id="e5a96-138">OUTPUTS</span></span>

### <span data-ttu-id="e5a96-139">WindowsAzure, EffectiveRouteTable, WindowsAzure에 대 한 system.webserver<. a. a. m a. 네트워크></span><span class="sxs-lookup"><span data-stu-id="e5a96-139">System.Collections.Generic.IEnumerable<Microsoft.WindowsAzure.Management.Network.Models.EffectiveRouteTable, Microsoft.WindowsAzure.Management.Network></span></span>

## <span data-ttu-id="e5a96-140">상속자</span><span class="sxs-lookup"><span data-stu-id="e5a96-140">NOTES</span></span>

## <span data-ttu-id="e5a96-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5a96-141">RELATED LINKS</span></span>

[<span data-ttu-id="e5a96-142">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5a96-142">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="e5a96-143">새로운 AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5a96-143">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="e5a96-144">제거-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5a96-144">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)

[<span data-ttu-id="e5a96-145">제거-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5a96-145">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="e5a96-146">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5a96-146">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


