---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
ms.openlocfilehash: 3e42cf7c2be8433d9e1b7e85987e53b9f0050038
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882361"
---
# <span data-ttu-id="03820-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="03820-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="03820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03820-102">SYNOPSIS</span></span>
<span data-ttu-id="03820-103">구성할 수 있는 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03820-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03820-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03820-104">SYNTAX</span></span>

### <span data-ttu-id="03820-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="03820-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03820-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="03820-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03820-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="03820-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03820-108">설명은</span><span class="sxs-lookup"><span data-stu-id="03820-108">DESCRIPTION</span></span>
<span data-ttu-id="03820-109">**AzureRmVMConfig** Cmdlet은 Azure에 대해 구성할 수 있는 로컬 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03820-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="03820-110">다른 cmdlet을 사용 하 여 AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, Set-AzureRmVMOSDisk 등의 가상 컴퓨터 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03820-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="03820-111">예제의</span><span class="sxs-lookup"><span data-stu-id="03820-111">EXAMPLES</span></span>

### <span data-ttu-id="03820-112">예제 1: 가상 컴퓨터 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="03820-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="03820-113">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="03820-114">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="03820-115">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="03820-116">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="03820-117">변수</span><span class="sxs-lookup"><span data-stu-id="03820-117">PARAMETERS</span></span>

### <span data-ttu-id="03820-118">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="03820-118">-AssignIdentity</span></span>
<span data-ttu-id="03820-119">시스템에서 가상 컴퓨터용으로 할당 된 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03820-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="03820-120">-AvailabilitySetId</span></span>
<span data-ttu-id="03820-121">가용성 집합의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="03820-122">가용성 집합 개체를 가져오려면 Get-AzureRmAvailabilitySet cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="03820-123">가용성 집합 개체에 ID 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03820-123">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03820-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03820-124">-DefaultProfile</span></span>
<span data-ttu-id="03820-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03820-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03820-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="03820-126">-IdentityId</span></span>
<span data-ttu-id="03820-127">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="03820-128">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03820-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="03820-129">-IdentityType</span></span>
<span data-ttu-id="03820-130">가상 컴퓨터의 id입니다 (구성 된 경우).</span><span class="sxs-lookup"><span data-stu-id="03820-130">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03820-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="03820-131">-LicenseType</span></span>
<span data-ttu-id="03820-132">라이선스 형식-고유한 라이선스 시나리오를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="03820-132">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03820-133">태그</span><span class="sxs-lookup"><span data-stu-id="03820-133">-Tags</span></span>
<span data-ttu-id="03820-134">리소스에 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="03820-134">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03820-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="03820-135">-VMName</span></span>
<span data-ttu-id="03820-136">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03820-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="03820-137">-VMSize</span></span>
<span data-ttu-id="03820-138">가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-138">Specifies the size for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03820-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="03820-139">-Zone</span></span>
<span data-ttu-id="03820-140">가상 컴퓨터의 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-140">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03820-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03820-141">CommonParameters</span></span>
<span data-ttu-id="03820-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03820-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03820-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03820-144">입력</span><span class="sxs-lookup"><span data-stu-id="03820-144">INPUTS</span></span>

### <span data-ttu-id="03820-145">않아야</span><span class="sxs-lookup"><span data-stu-id="03820-145">None</span></span>
<span data-ttu-id="03820-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03820-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03820-147">출력</span><span class="sxs-lookup"><span data-stu-id="03820-147">OUTPUTS</span></span>

### <span data-ttu-id="03820-148">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="03820-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="03820-149">상속자</span><span class="sxs-lookup"><span data-stu-id="03820-149">NOTES</span></span>

## <span data-ttu-id="03820-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03820-150">RELATED LINKS</span></span>

[<span data-ttu-id="03820-151">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="03820-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="03820-152">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="03820-152">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="03820-153">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="03820-153">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="03820-154">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="03820-154">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


