---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: cadcaccc2bb93dee5298ca92561c5bef36b5d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537379"
---
# <span data-ttu-id="d5d9e-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d5d9e-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="d5d9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d9e-103">가상 컴퓨터를 VMImage로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5d9e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5d9e-104">SYNTAX</span></span>

### <span data-ttu-id="d5d9e-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5d9e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5d9e-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d5d9e-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5d9e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d5d9e-107">DESCRIPTION</span></span>
<span data-ttu-id="d5d9e-108">**AzureRmVMImage** cmdlet은 가상 컴퓨터를 VMImage로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="d5d9e-109">가상 컴퓨터 이미지를 만들기 전에 가상 컴퓨터를 sysprep 하 고 Set-AzureRmVM cmdlet을 사용 하 여 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="d5d9e-110">이 cmdlet의 출력은 JSON (JavaScript 개체 표기법) 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="d5d9e-111">캡처한 이미지에서 가상 컴퓨터를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="d5d9e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d5d9e-112">EXAMPLES</span></span>

### <span data-ttu-id="d5d9e-113">예제 1: 가상 컴퓨터 캡처</span><span class="sxs-lookup"><span data-stu-id="d5d9e-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="d5d9e-114">첫 번째 명령은 VirtualMachine07 이라는 가상 컴퓨터를 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="d5d9e-115">두 번째 명령은 VirtualMachine07 이라는 가상 컴퓨터를 VMImage로 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="d5d9e-116">**Output** 속성은 JSON 템플릿을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="d5d9e-117">변수</span><span class="sxs-lookup"><span data-stu-id="d5d9e-117">PARAMETERS</span></span>

### <span data-ttu-id="d5d9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d9e-118">-DefaultProfile</span></span>
<span data-ttu-id="d5d9e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5d9e-120">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="d5d9e-120">-DestinationContainerName</span></span>
<span data-ttu-id="d5d9e-121">"시스템" 컨테이너 내에서 이미지를 포함 하려는 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-121">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="d5d9e-122">컨테이너가 없는 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-122">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="d5d9e-123">VMImage를 구성 하는 Vhd (가상 하드 디스크)는이 매개 변수에서 지정 하는 컨테이너에 위치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-123">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="d5d9e-124">Vhd가 여러 저장소 계정에 걸쳐 분산 되어 있는 경우이 cmdlet은 각 저장소 계정에이 이름을 가진 하나의 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-124">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="d5d9e-125">저장 된 이미지의 URL은 다음과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-125">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="d5d9e-126"> https://. \<storageAccountName\> blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> . / \<vhdPrefix-osDisk\></span><span class="sxs-lookup"><span data-stu-id="d5d9e-126">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="d5d9e-127">-Id</span><span class="sxs-lookup"><span data-stu-id="d5d9e-127">-Id</span></span>
<span data-ttu-id="d5d9e-128">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-128">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="d5d9e-129">-이름</span><span class="sxs-lookup"><span data-stu-id="d5d9e-129">-Name</span></span>
<span data-ttu-id="d5d9e-130">이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-130">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d9e-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="d5d9e-131">-Overwrite</span></span>
<span data-ttu-id="d5d9e-132">이 cmdlet이 대상 컨테이너에서 동일한 접두사를 가진 Vhd를 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-132">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="d5d9e-133">-Path</span><span class="sxs-lookup"><span data-stu-id="d5d9e-133">-Path</span></span>
<span data-ttu-id="d5d9e-134">VHD의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-134">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="d5d9e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d9e-135">-ResourceGroupName</span></span>
<span data-ttu-id="d5d9e-136">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-136">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d5d9e-137">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="d5d9e-137">-VHDNamePrefix</span></span>
<span data-ttu-id="d5d9e-138">VMImage의 저장소 프로필을 구성 하는 blob 이름에 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-138">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="d5d9e-139">예를 들어 운영 체제 디스크에 대 한 접두사 vhdPrefix는 vhdPrefix-osdisk .와 같은 이름으로 \<guid\> 반환 됩니다. .vhd.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-139">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="d5d9e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d9e-140">CommonParameters</span></span>
<span data-ttu-id="d5d9e-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d9e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d9e-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5d9e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d9e-143">입력</span><span class="sxs-lookup"><span data-stu-id="d5d9e-143">INPUTS</span></span>

## <span data-ttu-id="d5d9e-144">출력</span><span class="sxs-lookup"><span data-stu-id="d5d9e-144">OUTPUTS</span></span>

## <span data-ttu-id="d5d9e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="d5d9e-145">NOTES</span></span>

## <span data-ttu-id="d5d9e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5d9e-146">RELATED LINKS</span></span>

[<span data-ttu-id="d5d9e-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d5d9e-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="d5d9e-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d5d9e-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="d5d9e-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d5d9e-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="d5d9e-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d5d9e-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="d5d9e-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d5d9e-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)

