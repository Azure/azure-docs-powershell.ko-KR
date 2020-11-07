---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b663087437097b3e059f9d88c7720696222134e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868922"
---
# <span data-ttu-id="68cd0-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="68cd0-101">Save-AzVMImage</span></span>

## <span data-ttu-id="68cd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="68cd0-103">가상 컴퓨터를 VMImage로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="68cd0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68cd0-104">SYNTAX</span></span>

### <span data-ttu-id="68cd0-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="68cd0-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68cd0-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="68cd0-106">IdParameterSetName</span></span>
```
Save-AzVMImage [[-Name] <String>] [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68cd0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="68cd0-107">DESCRIPTION</span></span>
<span data-ttu-id="68cd0-108">**AzVMImage** cmdlet은 가상 컴퓨터를 VMImage로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="68cd0-109">가상 컴퓨터 이미지를 만들기 전에 가상 컴퓨터를 sysprep 하 고 Set-AzVM cmdlet을 사용 하 여 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="68cd0-110">이 cmdlet의 출력은 JSON (JavaScript 개체 표기법) 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="68cd0-111">캡처한 이미지에서 가상 컴퓨터를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="68cd0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="68cd0-112">EXAMPLES</span></span>

### <span data-ttu-id="68cd0-113">예제 1: 가상 컴퓨터 캡처</span><span class="sxs-lookup"><span data-stu-id="68cd0-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="68cd0-114">첫 번째 명령은 VirtualMachine07 이라는 가상 컴퓨터를 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="68cd0-115">두 번째 명령은 VirtualMachine07 이라는 가상 컴퓨터를 VMImage로 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="68cd0-116">**Output** 속성은 JSON 템플릿을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="68cd0-117">변수</span><span class="sxs-lookup"><span data-stu-id="68cd0-117">PARAMETERS</span></span>

### <span data-ttu-id="68cd0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68cd0-118">-AsJob</span></span>
<span data-ttu-id="68cd0-119">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="68cd0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cd0-120">-DefaultProfile</span></span>
<span data-ttu-id="68cd0-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68cd0-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="68cd0-122">-DestinationContainerName</span></span>
<span data-ttu-id="68cd0-123">"시스템" 컨테이너 내에서 이미지를 포함 하려는 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="68cd0-124">컨테이너가 없는 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="68cd0-125">VMImage를 구성 하는 Vhd (가상 하드 디스크)는이 매개 변수에서 지정 하는 컨테이너에 위치 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="68cd0-126">Vhd가 여러 저장소 계정에 걸쳐 분산 되어 있는 경우이 cmdlet은 각 저장소 계정에이 이름을 가진 하나의 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="68cd0-127">저장 된 이미지의 URL은 https:// \< storageaccountname \> . blob.core.windows.net/system/Microsoft.Compute/Images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> . i a y와 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="68cd0-128">-Id</span><span class="sxs-lookup"><span data-stu-id="68cd0-128">-Id</span></span>
<span data-ttu-id="68cd0-129">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="68cd0-130">-이름</span><span class="sxs-lookup"><span data-stu-id="68cd0-130">-Name</span></span>
<span data-ttu-id="68cd0-131">이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-131">Specifies a name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68cd0-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="68cd0-132">-Overwrite</span></span>
<span data-ttu-id="68cd0-133">이 cmdlet이 대상 컨테이너에서 동일한 접두사를 가진 Vhd를 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="68cd0-134">-Path</span><span class="sxs-lookup"><span data-stu-id="68cd0-134">-Path</span></span>
<span data-ttu-id="68cd0-135">캡처한 이미지의 템플릿이 저장 되는 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="68cd0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68cd0-136">-ResourceGroupName</span></span>
<span data-ttu-id="68cd0-137">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="68cd0-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="68cd0-138">-VHDNamePrefix</span></span>
<span data-ttu-id="68cd0-139">VMImage의 저장소 프로필을 구성 하는 blob 이름에 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="68cd0-140">예를 들어 운영 체제 디스크의 접두사 vhdPrefix는 name vhdPrefix-osdisk로 반환 됩니다. \< guid.empty \> .</span><span class="sxs-lookup"><span data-stu-id="68cd0-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="68cd0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cd0-141">CommonParameters</span></span>
<span data-ttu-id="68cd0-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cd0-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68cd0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cd0-144">입력</span><span class="sxs-lookup"><span data-stu-id="68cd0-144">INPUTS</span></span>

### <span data-ttu-id="68cd0-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68cd0-145">System.String</span></span>

### <span data-ttu-id="68cd0-146">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="68cd0-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68cd0-147">출력</span><span class="sxs-lookup"><span data-stu-id="68cd0-147">OUTPUTS</span></span>

### <span data-ttu-id="68cd0-148">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="68cd0-149">상속자</span><span class="sxs-lookup"><span data-stu-id="68cd0-149">NOTES</span></span>

## <span data-ttu-id="68cd0-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68cd0-150">RELATED LINKS</span></span>

[<span data-ttu-id="68cd0-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="68cd0-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="68cd0-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="68cd0-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="68cd0-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="68cd0-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="68cd0-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="68cd0-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="68cd0-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="68cd0-155">Set-AzVM</span></span>](./Set-AzVM.md)


