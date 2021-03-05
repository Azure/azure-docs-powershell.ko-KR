---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: d979e89583b19270dfd13bae85a3afe1505ed55e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998209"
---
# <span data-ttu-id="806d5-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="806d5-101">Save-AzVMImage</span></span>

## <span data-ttu-id="806d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="806d5-102">SYNOPSIS</span></span>
<span data-ttu-id="806d5-103">가상 머신을 VMImage로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="806d5-104">구문</span><span class="sxs-lookup"><span data-stu-id="806d5-104">SYNTAX</span></span>

### <span data-ttu-id="806d5-105">ResourceGroupNameParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="806d5-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="806d5-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="806d5-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="806d5-107">설명</span><span class="sxs-lookup"><span data-stu-id="806d5-107">DESCRIPTION</span></span>
<span data-ttu-id="806d5-108">**Save-AzVMImage** cmdlet은 가상 머신을 VMImage로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="806d5-109">가상 머신 이미지를 만들기 전에 가상 머신을 sysprep한 다음, Set-AzVM cmdlet을 사용하여 일반화된 것으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="806d5-110">이 cmdlet의 출력은 JSON(JavaScript 개체 표시) 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="806d5-111">캡처된 이미지에서 가상 머신을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="806d5-112">예제</span><span class="sxs-lookup"><span data-stu-id="806d5-112">EXAMPLES</span></span>

### <span data-ttu-id="806d5-113">예제 1: 가상 머신 캡처</span><span class="sxs-lookup"><span data-stu-id="806d5-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="806d5-114">첫 번째 명령은 VirtualMachine07이라는 가상 머신을 일반화된 것으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="806d5-115">두 번째 명령은 VMImage로 VirtualMachine07이라는 가상 머신을 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="806d5-116">Output **속성은** JSON 템플릿을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="806d5-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="806d5-117">PARAMETERS</span></span>

### <span data-ttu-id="806d5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="806d5-118">-AsJob</span></span>
<span data-ttu-id="806d5-119">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806d5-120">-DefaultProfile</span></span>
<span data-ttu-id="806d5-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806d5-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="806d5-122">-DestinationContainerName</span></span>
<span data-ttu-id="806d5-123">이미지를 보관할 "시스템" 컨테이너 내부에 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="806d5-124">컨테이너가 없는 경우 해당 컨테이너가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="806d5-125">VMImage를 구성하는 VHD(가상 하드 디스크)는 이 매개 변수가 지정하는 컨테이너에 상주합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="806d5-126">VHD가 여러 저장소 계정에 분산된 경우 이 cmdlet은 각 저장소 계정에 이 이름이 있는 하나의 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="806d5-127">저장된 이미지의 URL은 \<storageAccountName\> blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> .https:// .xxxx-xxxx-xx-x.vhd-https://.xx</span><span class="sxs-lookup"><span data-stu-id="806d5-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806d5-128">-Id</span><span class="sxs-lookup"><span data-stu-id="806d5-128">-Id</span></span>
<span data-ttu-id="806d5-129">가상 머신의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-129">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806d5-130">-Name</span><span class="sxs-lookup"><span data-stu-id="806d5-130">-Name</span></span>
<span data-ttu-id="806d5-131">이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806d5-132">-덮어 덮어 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="806d5-132">-Overwrite</span></span>
<span data-ttu-id="806d5-133">이 cmdlet은 대상 컨테이너에 동일한 도두가 있는 모든 VHD를 덮어 덮어 웁니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806d5-134">-Path</span><span class="sxs-lookup"><span data-stu-id="806d5-134">-Path</span></span>
<span data-ttu-id="806d5-135">캡처된 이미지의 템플릿이 저장되는 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-135">The file path in which the template of the captured image is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806d5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="806d5-136">-ResourceGroupName</span></span>
<span data-ttu-id="806d5-137">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806d5-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="806d5-138">-VHDNamePrefix</span></span>
<span data-ttu-id="806d5-139">VMImage의 저장소 프로필을 구성하는 Blob의 이름으로 도두를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="806d5-140">예를 들어 운영 체제 디스크에 대한 vhdPrefix는 이름 vhdPrefix-osdisk입니다. \<guid\> . vhd.</span><span class="sxs-lookup"><span data-stu-id="806d5-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806d5-141">CommonParameters</span></span>
<span data-ttu-id="806d5-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="806d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806d5-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="806d5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806d5-144">입력</span><span class="sxs-lookup"><span data-stu-id="806d5-144">INPUTS</span></span>

### <span data-ttu-id="806d5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="806d5-145">System.String</span></span>

### <span data-ttu-id="806d5-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="806d5-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="806d5-147">출력</span><span class="sxs-lookup"><span data-stu-id="806d5-147">OUTPUTS</span></span>

### <span data-ttu-id="806d5-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="806d5-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="806d5-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="806d5-149">NOTES</span></span>

## <span data-ttu-id="806d5-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="806d5-150">RELATED LINKS</span></span>

[<span data-ttu-id="806d5-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="806d5-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="806d5-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="806d5-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="806d5-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="806d5-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="806d5-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="806d5-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="806d5-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="806d5-155">Set-AzVM</span></span>](./Set-AzVM.md)


