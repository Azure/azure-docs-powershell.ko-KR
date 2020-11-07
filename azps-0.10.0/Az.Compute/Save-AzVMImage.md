---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b01f8d356d83cb111441cf911750056033422fe8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876920"
---
# <span data-ttu-id="3af58-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3af58-101">Save-AzVMImage</span></span>

## <span data-ttu-id="3af58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3af58-102">SYNOPSIS</span></span>
<span data-ttu-id="3af58-103">가상 컴퓨터를 VMImage로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="3af58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3af58-104">SYNTAX</span></span>

### <span data-ttu-id="3af58-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3af58-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3af58-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3af58-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3af58-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3af58-107">DESCRIPTION</span></span>
<span data-ttu-id="3af58-108">**AzVMImage** cmdlet은 가상 컴퓨터를 VMImage로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="3af58-109">가상 컴퓨터 이미지를 만들기 전에 가상 컴퓨터를 sysprep 하 고 Set-AzVM cmdlet을 사용 하 여 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>

<span data-ttu-id="3af58-110">이 cmdlet의 출력은 JSON (JavaScript 개체 표기법) 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="3af58-111">캡처한 이미지에서 가상 컴퓨터를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="3af58-112">예제의</span><span class="sxs-lookup"><span data-stu-id="3af58-112">EXAMPLES</span></span>

### <span data-ttu-id="3af58-113">예제 1: 가상 컴퓨터 캡처</span><span class="sxs-lookup"><span data-stu-id="3af58-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="3af58-114">첫 번째 명령은 VirtualMachine07 이라는 가상 컴퓨터를 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="3af58-115">두 번째 명령은 VirtualMachine07 이라는 가상 컴퓨터를 VMImage로 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="3af58-116">**Output** 속성은 JSON 템플릿을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="3af58-117">변수</span><span class="sxs-lookup"><span data-stu-id="3af58-117">PARAMETERS</span></span>

### <span data-ttu-id="3af58-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3af58-118">-AsJob</span></span>
<span data-ttu-id="3af58-119">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3af58-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af58-120">-DefaultProfile</span></span>
<span data-ttu-id="3af58-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3af58-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="3af58-122">-DestinationContainerName</span></span>
<span data-ttu-id="3af58-123">"시스템" 컨테이너 내에서 이미지를 포함 하려는 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="3af58-124">컨테이너가 없는 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="3af58-125">VMImage를 구성 하는 Vhd (가상 하드 디스크)는이 매개 변수에서 지정 하는 컨테이너에 위치 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="3af58-126">Vhd가 여러 저장소 계정에 걸쳐 분산 되어 있는 경우이 cmdlet은 각 저장소 계정에이 이름을 가진 하나의 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="3af58-127">저장 된 이미지의 URL은 다음과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="3af58-128"> https:// \< storageaccountname \> . blob.core.windows.net/system/Microsoft.Compute/Images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> .</span><span class="sxs-lookup"><span data-stu-id="3af58-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af58-129">-Id</span><span class="sxs-lookup"><span data-stu-id="3af58-129">-Id</span></span>
<span data-ttu-id="3af58-130">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-130">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af58-131">-이름</span><span class="sxs-lookup"><span data-stu-id="3af58-131">-Name</span></span>
<span data-ttu-id="3af58-132">이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-132">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af58-133">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="3af58-133">-Overwrite</span></span>
<span data-ttu-id="3af58-134">이 cmdlet이 대상 컨테이너에서 동일한 접두사를 가진 Vhd를 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af58-135">-Path</span><span class="sxs-lookup"><span data-stu-id="3af58-135">-Path</span></span>
<span data-ttu-id="3af58-136">VHD의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-136">Specifies the path of the VHD.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af58-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af58-137">-ResourceGroupName</span></span>
<span data-ttu-id="3af58-138">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-138">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af58-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="3af58-139">-VHDNamePrefix</span></span>
<span data-ttu-id="3af58-140">VMImage의 저장소 프로필을 구성 하는 blob 이름에 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="3af58-141">예를 들어 운영 체제 디스크의 접두사 vhdPrefix는 name vhdPrefix-osdisk로 반환 됩니다. \< guid.empty \> .</span><span class="sxs-lookup"><span data-stu-id="3af58-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af58-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af58-142">CommonParameters</span></span>
<span data-ttu-id="3af58-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af58-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af58-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af58-145">입력</span><span class="sxs-lookup"><span data-stu-id="3af58-145">INPUTS</span></span>

### <span data-ttu-id="3af58-146">않아야</span><span class="sxs-lookup"><span data-stu-id="3af58-146">None</span></span>
<span data-ttu-id="3af58-147">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3af58-148">출력</span><span class="sxs-lookup"><span data-stu-id="3af58-148">OUTPUTS</span></span>

### <span data-ttu-id="3af58-149">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="3af58-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="3af58-150">상속자</span><span class="sxs-lookup"><span data-stu-id="3af58-150">NOTES</span></span>

## <span data-ttu-id="3af58-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3af58-151">RELATED LINKS</span></span>

[<span data-ttu-id="3af58-152">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3af58-152">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="3af58-153">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="3af58-153">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="3af58-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3af58-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="3af58-155">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="3af58-155">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="3af58-156">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="3af58-156">Set-AzVM</span></span>](./Set-AzVM.md)


