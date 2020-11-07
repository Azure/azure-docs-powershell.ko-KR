---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4b128346d77e090e5b0699ace8f03eaa9a4786a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876998"
---
# <span data-ttu-id="67705-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="67705-101">New-AzVMConfig</span></span>

## <span data-ttu-id="67705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67705-102">SYNOPSIS</span></span>
<span data-ttu-id="67705-103">구성할 수 있는 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67705-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="67705-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67705-104">SYNTAX</span></span>

### <span data-ttu-id="67705-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="67705-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67705-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="67705-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67705-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="67705-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67705-108">설명은</span><span class="sxs-lookup"><span data-stu-id="67705-108">DESCRIPTION</span></span>
<span data-ttu-id="67705-109">**AzVMConfig** Cmdlet은 Azure에 대해 구성할 수 있는 로컬 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67705-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="67705-110">다른 cmdlet을 사용 하 여 AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, Set-AzVMOSDisk 등의 가상 컴퓨터 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67705-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="67705-111">예제의</span><span class="sxs-lookup"><span data-stu-id="67705-111">EXAMPLES</span></span>

### <span data-ttu-id="67705-112">예제 1: 가상 컴퓨터 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="67705-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="67705-113">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="67705-114">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="67705-115">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="67705-116">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="67705-117">변수</span><span class="sxs-lookup"><span data-stu-id="67705-117">PARAMETERS</span></span>

### <span data-ttu-id="67705-118">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="67705-118">-AssignIdentity</span></span>
<span data-ttu-id="67705-119">시스템에서 가상 컴퓨터용으로 할당 된 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="67705-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="67705-120">-AvailabilitySetId</span></span>
<span data-ttu-id="67705-121">가용성 집합의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="67705-122">가용성 집합 개체를 가져오려면 Get-AzAvailabilitySet cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="67705-123">가용성 집합 개체에 ID 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67705-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="67705-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67705-124">-DefaultProfile</span></span>
<span data-ttu-id="67705-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67705-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67705-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="67705-126">-IdentityId</span></span>
<span data-ttu-id="67705-127">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="67705-128">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="67705-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="67705-129">-IdentityType</span></span>
<span data-ttu-id="67705-130">가상 컴퓨터의 id입니다 (구성 된 경우).</span><span class="sxs-lookup"><span data-stu-id="67705-130">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="67705-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="67705-131">-LicenseType</span></span>
<span data-ttu-id="67705-132">라이선스 형식-고유한 라이선스 시나리오를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67705-132">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="67705-133">태그</span><span class="sxs-lookup"><span data-stu-id="67705-133">-Tags</span></span>
<span data-ttu-id="67705-134">리소스에 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="67705-134">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="67705-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="67705-135">-VMName</span></span>
<span data-ttu-id="67705-136">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="67705-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="67705-137">-VMSize</span></span>
<span data-ttu-id="67705-138">가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-138">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="67705-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="67705-139">-Zone</span></span>
<span data-ttu-id="67705-140">가상 컴퓨터의 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-140">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="67705-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67705-141">CommonParameters</span></span>
<span data-ttu-id="67705-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67705-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67705-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67705-144">입력</span><span class="sxs-lookup"><span data-stu-id="67705-144">INPUTS</span></span>

### <span data-ttu-id="67705-145">않아야</span><span class="sxs-lookup"><span data-stu-id="67705-145">None</span></span>
<span data-ttu-id="67705-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67705-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67705-147">출력</span><span class="sxs-lookup"><span data-stu-id="67705-147">OUTPUTS</span></span>

### <span data-ttu-id="67705-148">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="67705-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="67705-149">상속자</span><span class="sxs-lookup"><span data-stu-id="67705-149">NOTES</span></span>

## <span data-ttu-id="67705-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67705-150">RELATED LINKS</span></span>

[<span data-ttu-id="67705-151">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="67705-151">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="67705-152">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="67705-152">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="67705-153">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="67705-153">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="67705-154">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="67705-154">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


