---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045956"
---
# <span data-ttu-id="504ec-101">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="504ec-101">Set-AzureIPForwarding</span></span>

## <span data-ttu-id="504ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="504ec-102">SYNOPSIS</span></span>
<span data-ttu-id="504ec-103">IP 전달을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-103">Enables or disables IP forwarding.</span></span>

## <span data-ttu-id="504ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="504ec-104">SYNTAX</span></span>

### <span data-ttu-id="504ec-105">EnableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="504ec-105">EnableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="504ec-106">DisableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="504ec-106">DisableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="504ec-107">EnableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="504ec-107">EnableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="504ec-108">DisableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="504ec-108">DisableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="504ec-109">설명은</span><span class="sxs-lookup"><span data-stu-id="504ec-109">DESCRIPTION</span></span>
<span data-ttu-id="504ec-110">**집합-AzureIPForwarding** cmdlet은 가상 컴퓨터에 대 한 IP 전달을 사용 하거나, 플랫폼을 서비스 (paas) 역할 또는 가상 컴퓨터 또는 PaaS 역할에 속한 네트워크 어댑터로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-110">The **Set-AzureIPForwarding** cmdlet enables or disables IP forwarding for a virtual machine, for a platform as a service (PaaS) role, or a network adapter that belongs to a virtual machine or PaaS role.</span></span>

## <span data-ttu-id="504ec-111">예제의</span><span class="sxs-lookup"><span data-stu-id="504ec-111">EXAMPLES</span></span>

### <span data-ttu-id="504ec-112">예제 1: 가상 컴퓨터에 대해 IP 전달 사용</span><span class="sxs-lookup"><span data-stu-id="504ec-112">Example 1: Enable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

<span data-ttu-id="504ec-113">이 명령은 ContosoService 이라는 서비스에 대 한 ContosoVM06 이라는 가상 컴퓨터를 가져오고 현재 cmdlet에 해당 가상 컴퓨터 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-113">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="504ec-114">현재 cmdlet은 해당 가상 컴퓨터에 대해 IP 전달을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-114">The current cmdlet enables IP forwarding for that virtual machine.</span></span>

### <span data-ttu-id="504ec-115">예제 2: 가상 컴퓨터에 대해 IP 전달 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="504ec-115">Example 2: Disable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

<span data-ttu-id="504ec-116">이 명령은 ContosoService 이라는 서비스에 대 한 ContosoVM06 이라는 가상 컴퓨터를 가져오고 현재 cmdlet에 해당 가상 컴퓨터 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-116">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="504ec-117">현재 cmdlet은 해당 가상 컴퓨터에 대 한 IP 전달을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-117">The current cmdlet disables IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="504ec-118">변수</span><span class="sxs-lookup"><span data-stu-id="504ec-118">PARAMETERS</span></span>

### <span data-ttu-id="504ec-119">-Disable</span><span class="sxs-lookup"><span data-stu-id="504ec-119">-Disable</span></span>
<span data-ttu-id="504ec-120">이 cmdlet이 IP 전달을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-120">Indicates that this cmdlet disables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504ec-121">-사용</span><span class="sxs-lookup"><span data-stu-id="504ec-121">-Enable</span></span>
<span data-ttu-id="504ec-122">이 cmdlet이 IP 전달을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-122">Indicates that this cmdlet enables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504ec-123">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="504ec-123">-NetworkInterfaceName</span></span>
<span data-ttu-id="504ec-124">이 cmdlet이 IP 전달을 설정 하는 네트워크 어댑터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-124">Specifies the name of the network adapter on which this cmdlet sets IP forwarding.</span></span>

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

### <span data-ttu-id="504ec-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="504ec-125">-PassThru</span></span>
<span data-ttu-id="504ec-126">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="504ec-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504ec-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="504ec-128">-Profile</span></span>
<span data-ttu-id="504ec-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="504ec-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="504ec-131">-RoleName</span><span class="sxs-lookup"><span data-stu-id="504ec-131">-RoleName</span></span>
<span data-ttu-id="504ec-132">이 cmdlet이 IP 전달을 설정 하는 PaaS 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-132">Specifies the name of a PaaS role on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="504ec-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="504ec-133">-ServiceName</span></span>
<span data-ttu-id="504ec-134">클라우드 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-134">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="504ec-135">PaaS 역할은이 매개 변수에서 지정 하는 서비스에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-135">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="504ec-136">-슬롯</span><span class="sxs-lookup"><span data-stu-id="504ec-136">-Slot</span></span>
<span data-ttu-id="504ec-137">PaaS 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-137">Specifies a PaaS slot.</span></span>
<span data-ttu-id="504ec-138">이 cmdlet에서 착신 전환을 설정 하는 PaaS 역할에는이 매개 변수에서 지정 하는 슬롯이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-138">The PaaS role for which this cmdlet sets forwarding has the slot that this parameter specifies.</span></span>
<span data-ttu-id="504ec-139">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-139">Valid values are:</span></span>

- <span data-ttu-id="504ec-140">프로덕션용</span><span class="sxs-lookup"><span data-stu-id="504ec-140">Production</span></span>
- <span data-ttu-id="504ec-141">대기</span><span class="sxs-lookup"><span data-stu-id="504ec-141">Staging</span></span>

<span data-ttu-id="504ec-142">기본값은 실제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-142">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504ec-143">-VM</span><span class="sxs-lookup"><span data-stu-id="504ec-143">-VM</span></span>
<span data-ttu-id="504ec-144">이 cmdlet이 IP 전달을 설정 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-144">Specifies the virtual machine object on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="504ec-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504ec-145">CommonParameters</span></span>
<span data-ttu-id="504ec-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="504ec-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504ec-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="504ec-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504ec-148">입력</span><span class="sxs-lookup"><span data-stu-id="504ec-148">INPUTS</span></span>

## <span data-ttu-id="504ec-149">출력</span><span class="sxs-lookup"><span data-stu-id="504ec-149">OUTPUTS</span></span>

### <span data-ttu-id="504ec-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="504ec-150">System.Boolean</span></span>

## <span data-ttu-id="504ec-151">상속자</span><span class="sxs-lookup"><span data-stu-id="504ec-151">NOTES</span></span>

## <span data-ttu-id="504ec-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="504ec-152">RELATED LINKS</span></span>

[<span data-ttu-id="504ec-153">Get-AzureIPForwarding 전환</span><span class="sxs-lookup"><span data-stu-id="504ec-153">Get-AzureIPForwarding</span></span>](./Get-AzureIPForwarding.md)
