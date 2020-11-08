---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsvmextension
schema: 2.0.0
ms.openlocfilehash: a9c5a207d478fe40181150206990cb47ad4e45d5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046929"
---
# <span data-ttu-id="38b03-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="38b03-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="38b03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38b03-102">SYNOPSIS</span></span>
<span data-ttu-id="38b03-103">Publisher 버전을 사용 하 여 가상 컴퓨터 확장 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-103">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="38b03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="38b03-104">SYNTAX</span></span>

### <span data-ttu-id="38b03-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="38b03-105">CreateExpanded (Default)</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-ComputeRole <String>] [-IsSystemExtension] [-PropertiesPublisher <String>]
 [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>] [-SupportMultipleExtensions]
 [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="38b03-106">만드는</span><span class="sxs-lookup"><span data-stu-id="38b03-106">Create</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> -Extension <IVMExtensionParameters>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="38b03-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="38b03-107">CreateViaIdentity</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> -Extension <IVMExtensionParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="38b03-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="38b03-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> [-Publisher <String>] [-ComputeRole <String>]
 [-IsSystemExtension] [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>]
 [-SupportMultipleExtensions] [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38b03-109">설명은</span><span class="sxs-lookup"><span data-stu-id="38b03-109">DESCRIPTION</span></span>
<span data-ttu-id="38b03-110">Publisher 버전을 사용 하 여 가상 컴퓨터 확장 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-110">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="38b03-111">예제의</span><span class="sxs-lookup"><span data-stu-id="38b03-111">EXAMPLES</span></span>

### <span data-ttu-id="38b03-112">예제 1: Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="38b03-112">Example 1: Add-AzsVMExtension</span></span>
```powershell
PS C:\> Add-AzsVMExtension -Location "local" -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"

ExtensionType            : MicroExtension
TypeHandlerVersion       : 0.1.0
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/local/artifactTypes/VMExtension/publishers/Microsoft/types/MicroExtension/versions/0.1.0
IsSystemExtension        : False
Location                 : local
Name                     :
ProvisioningState        : Creating
Publisher                : Microsoft
SourceBlobUri            : https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip
SupportMultipleExtension : True
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Linux
```

<span data-ttu-id="38b03-113">공용으로 액세스할 수 있는 링크를 사용 하 여 확장의 위치 또는 SasUri를 사용 하 여 Azure Blob에 대 한 URI를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-113">Use a publicly accessible link to provide the location of the extension, or the URI to an Azure Blob using the SasUri.</span></span>

## <span data-ttu-id="38b03-114">변수</span><span class="sxs-lookup"><span data-stu-id="38b03-114">PARAMETERS</span></span>

### <span data-ttu-id="38b03-115">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="38b03-115">-ComputeRole</span></span>
<span data-ttu-id="38b03-116">계산 역할</span><span class="sxs-lookup"><span data-stu-id="38b03-116">Compute role</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b03-117">-DefaultProfile</span></span>
<span data-ttu-id="38b03-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-119">-확장</span><span class="sxs-lookup"><span data-stu-id="38b03-119">-Extension</span></span>
<span data-ttu-id="38b03-120">새 가상 컴퓨터 확장 이미지를 만드는 데 사용 되는 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-120">Parameters used to create a new Virtual Machine Extension Image.</span></span>
<span data-ttu-id="38b03-121">생성 하려면 확장 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-121">To construct, see NOTES section for EXTENSION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38b03-122">-InputObject</span></span>
<span data-ttu-id="38b03-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-124">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="38b03-124">-IsSystemExtension</span></span>
<span data-ttu-id="38b03-125">시스템에 대 한 내선 번호 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-125">Indicates if the extension is for the system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-126">-위치</span><span class="sxs-lookup"><span data-stu-id="38b03-126">-Location</span></span>
<span data-ttu-id="38b03-127">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-128">-속성 게시자</span><span class="sxs-lookup"><span data-stu-id="38b03-128">-PropertiesPublisher</span></span>
<span data-ttu-id="38b03-129">VM 확장의 게시자</span><span class="sxs-lookup"><span data-stu-id="38b03-129">The publisher of the VM Extension</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-130">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="38b03-130">-ProvisioningState</span></span>
<span data-ttu-id="38b03-131">확장의 프로 비전 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-131">Provisioning state of extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="38b03-132">-Publisher</span></span>
<span data-ttu-id="38b03-133">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-133">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-134">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="38b03-134">-SourceBlob</span></span>
<span data-ttu-id="38b03-135">Azure 또는 AzureStack blob에 대 한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-135">URI to Azure or AzureStack blob.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38b03-136">-SubscriptionId</span></span>
<span data-ttu-id="38b03-137">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="38b03-138">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-139">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="38b03-139">-SupportMultipleExtensions</span></span>
<span data-ttu-id="38b03-140">여러 확장명을 지 원하는 경우 True입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-140">True if supports multiple extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-141">-Type</span><span class="sxs-lookup"><span data-stu-id="38b03-141">-Type</span></span>
<span data-ttu-id="38b03-142">확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-142">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-143">-버전</span><span class="sxs-lookup"><span data-stu-id="38b03-143">-Version</span></span>
<span data-ttu-id="38b03-144">리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-144">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-145">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="38b03-145">-VmOsType</span></span>
<span data-ttu-id="38b03-146">확장 처리기를 배포 하는 데 필요한 대상 가상 컴퓨터 운영 체제 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-146">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-147">-VMScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="38b03-147">-VMScaleSetEnabled</span></span>
<span data-ttu-id="38b03-148">확장을 가상 컴퓨터 확장 집합 지원에 사용할 수 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-148">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="38b03-149">-확인</span><span class="sxs-lookup"><span data-stu-id="38b03-149">-Confirm</span></span>
<span data-ttu-id="38b03-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b03-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b03-151">-WhatIf</span></span>
<span data-ttu-id="38b03-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38b03-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38b03-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b03-154">CommonParameters</span></span>
<span data-ttu-id="38b03-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b03-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="38b03-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b03-157">입력</span><span class="sxs-lookup"><span data-stu-id="38b03-157">INPUTS</span></span>

### <span data-ttu-id="38b03-158">Api20151201Preview Mextensiona. t t t. a t t.</span><span class="sxs-lookup"><span data-stu-id="38b03-158">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters</span></span>

### <span data-ttu-id="38b03-159">IComputeAdminIdentity (Microsoft. PowerShell. t t t)</span><span class="sxs-lookup"><span data-stu-id="38b03-159">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="38b03-160">출력</span><span class="sxs-lookup"><span data-stu-id="38b03-160">OUTPUTS</span></span>

### <span data-ttu-id="38b03-161">Api20151201Preview-. a t t. t t m 확장명</span><span class="sxs-lookup"><span data-stu-id="38b03-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="38b03-162">상속자</span><span class="sxs-lookup"><span data-stu-id="38b03-162">NOTES</span></span>

<span data-ttu-id="38b03-163">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-163">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38b03-164">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="38b03-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="38b03-165">확장 <IVMExtensionParameters> : 새 가상 컴퓨터 확장 이미지를 만드는 데 사용 되는 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-165">EXTENSION <IVMExtensionParameters>: Parameters used to create a new Virtual Machine Extension Image.</span></span>
  - <span data-ttu-id="38b03-166">`[ComputeRole <String>]`: 계산 역할</span><span class="sxs-lookup"><span data-stu-id="38b03-166">`[ComputeRole <String>]`: Compute role</span></span>
  - <span data-ttu-id="38b03-167">`[IsSystemExtension <Boolean?>]`: 확장을 시스템에 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-167">`[IsSystemExtension <Boolean?>]`: Indicates if the extension is for the system.</span></span>
  - <span data-ttu-id="38b03-168">`[ProvisioningState <ProvisioningState?>]`: 확장의 프로 비전 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of extension.</span></span>
  - <span data-ttu-id="38b03-169">`[Publisher <String>]`: VM 확장의 게시자</span><span class="sxs-lookup"><span data-stu-id="38b03-169">`[Publisher <String>]`: The publisher of the VM Extension</span></span>
  - <span data-ttu-id="38b03-170">`[SourceBlobUri <String>]`: URI에서 Azure 또는 AzureStack blob로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-170">`[SourceBlobUri <String>]`: URI to Azure or AzureStack blob.</span></span>
  - <span data-ttu-id="38b03-171">`[SupportMultipleExtension <Boolean?>]`: True 이면 여러 확장을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-171">`[SupportMultipleExtension <Boolean?>]`: True if supports multiple extensions.</span></span>
  - <span data-ttu-id="38b03-172">`[VMScaleSetEnabled <Boolean?>]`: 확장을 가상 컴퓨터 확장 집합 지원에 사용할 수 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-172">`[VMScaleSetEnabled <Boolean?>]`: Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>
  - <span data-ttu-id="38b03-173">`[VmosType <OSType?>]`: 확장 처리기를 배포 하는 데 필요한 대상 가상 컴퓨터 운영 체제 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-173">`[VmosType <OSType?>]`: Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

<span data-ttu-id="38b03-174">INPUTOBJECT <IComputeAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="38b03-174">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38b03-175">`[DiskId <String>]`: 디스크 guid를 id로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-175">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="38b03-176">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="38b03-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38b03-177">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-177">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="38b03-178">`[MigrationId <String>]`: 마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-178">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="38b03-179">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-179">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="38b03-180">`[Publisher <String>]`: 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-180">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="38b03-181">`[QuotaName <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-181">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="38b03-182">`[Sku <String>]`: SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-182">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="38b03-183">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-183">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="38b03-184">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-184">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="38b03-185">`[Type <String>]`: 확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-185">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="38b03-186">`[Version <String>]`: 리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="38b03-186">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="38b03-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38b03-187">RELATED LINKS</span></span>

