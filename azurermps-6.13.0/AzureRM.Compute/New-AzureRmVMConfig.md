---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 6809088110944648781fc2264bd2c56f98cbee1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532082"
---
# <span data-ttu-id="fdf44-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="fdf44-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="fdf44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdf44-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf44-103">구성할 수 있는 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdf44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fdf44-104">SYNTAX</span></span>

### <span data-ttu-id="fdf44-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fdf44-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdf44-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdf44-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdf44-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdf44-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf44-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fdf44-108">DESCRIPTION</span></span>
<span data-ttu-id="fdf44-109">**AzureRmVMConfig** Cmdlet은 Azure에 대해 구성할 수 있는 로컬 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="fdf44-110">다른 cmdlet을 사용 하 여 AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, Set-AzureRmVMOSDisk 등의 가상 컴퓨터 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="fdf44-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fdf44-111">EXAMPLES</span></span>

### <span data-ttu-id="fdf44-112">예제 1: 가상 컴퓨터 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="fdf44-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="fdf44-113">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="fdf44-114">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fdf44-115">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="fdf44-116">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="fdf44-117">변수</span><span class="sxs-lookup"><span data-stu-id="fdf44-117">PARAMETERS</span></span>

### <span data-ttu-id="fdf44-118">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="fdf44-118">-AssignIdentity</span></span>
<span data-ttu-id="fdf44-119">시스템에서 가상 컴퓨터용으로 할당 된 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf44-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="fdf44-120">-AvailabilitySetId</span></span>
<span data-ttu-id="fdf44-121">가용성 집합의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="fdf44-122">가용성 집합 개체를 가져오려면 Get-AzureRmAvailabilitySet cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="fdf44-123">가용성 집합 개체에 ID 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-123">The availability set object contains an ID property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf44-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf44-124">-DefaultProfile</span></span>
<span data-ttu-id="fdf44-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdf44-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="fdf44-126">-EnableUltraSSD</span></span>
<span data-ttu-id="fdf44-127">하나 이상의 관리 되는 데이터 디스크를 VM의 UltraSSD_LRS 저장소 계정 유형과 함께 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="fdf44-128">저장소 계정 유형이 UltraSSD_LRS 인 관리 디스크는이 속성을 사용 하도록 설정한 경우에만 가상 컴퓨터에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf44-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="fdf44-129">-IdentityId</span></span>
<span data-ttu-id="fdf44-130">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="fdf44-131">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf44-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="fdf44-132">-IdentityType</span></span>
<span data-ttu-id="fdf44-133">가상 컴퓨터의 id입니다 (구성 된 경우).</span><span class="sxs-lookup"><span data-stu-id="fdf44-133">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf44-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fdf44-134">-LicenseType</span></span>
<span data-ttu-id="fdf44-135">라이선스 형식-고유한 라이선스 시나리오를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-135">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf44-136">태그</span><span class="sxs-lookup"><span data-stu-id="fdf44-136">-Tags</span></span>
<span data-ttu-id="fdf44-137">리소스에 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-137">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf44-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="fdf44-138">-VMName</span></span>
<span data-ttu-id="fdf44-139">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-139">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf44-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="fdf44-140">-VMSize</span></span>
<span data-ttu-id="fdf44-141">가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-141">Specifies the size for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf44-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="fdf44-142">-Zone</span></span>
<span data-ttu-id="fdf44-143">가상 컴퓨터의 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-143">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf44-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf44-144">CommonParameters</span></span>
<span data-ttu-id="fdf44-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf44-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf44-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf44-147">입력</span><span class="sxs-lookup"><span data-stu-id="fdf44-147">INPUTS</span></span>

### <span data-ttu-id="fdf44-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fdf44-148">System.String</span></span>

### <span data-ttu-id="fdf44-149">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="fdf44-149">System.String[]</span></span>

### <span data-ttu-id="fdf44-150">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="fdf44-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fdf44-151">출력</span><span class="sxs-lookup"><span data-stu-id="fdf44-151">OUTPUTS</span></span>

### <span data-ttu-id="fdf44-152">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf44-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fdf44-153">상속자</span><span class="sxs-lookup"><span data-stu-id="fdf44-153">NOTES</span></span>

## <span data-ttu-id="fdf44-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdf44-154">RELATED LINKS</span></span>

[<span data-ttu-id="fdf44-155">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fdf44-155">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="fdf44-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="fdf44-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="fdf44-157">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="fdf44-157">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="fdf44-158">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fdf44-158">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


