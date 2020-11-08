---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DECCEE-86C8-4662-9ED0-D1BDB4E687C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68efd1c750646abffa90eb8318d0df189a4c9eb9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045715"
---
# <span data-ttu-id="2a9d1-101">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="2a9d1-101">Add-AzureVMImage</span></span>

## <span data-ttu-id="2a9d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a9d1-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9d1-103">새 운영 체제 이미지 또는 새 가상 컴퓨터 이미지를 이미지 리포지토리에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-103">Adds a new operating system image or a new virtual machine image to the image repository.</span></span>

## <span data-ttu-id="2a9d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a9d1-104">SYNTAX</span></span>

### <span data-ttu-id="2a9d1-105">OSImage (기본값)</span><span class="sxs-lookup"><span data-stu-id="2a9d1-105">OSImage (Default)</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-MediaLocation] <String> [-OS] <String> [[-Label] <String>]
 [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>]
 [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>] [[-SmallIconName] <String>]
 [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2a9d1-106">VMImage</span><span class="sxs-lookup"><span data-stu-id="2a9d1-106">VMImage</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-OS] <String>]
 [[-Label] <String>] [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>]
 [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2a9d1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2a9d1-107">DESCRIPTION</span></span>
<span data-ttu-id="2a9d1-108">**Add-AzureVMImage** cmdlet은 새 운영 체제 이미지 또는 새 가상 컴퓨터 이미지를 이미지 리포지토리에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-108">The **Add-AzureVMImage** cmdlet adds a new operating system image or a new virtual machine image to the image repository.</span></span>
<span data-ttu-id="2a9d1-109">이미지는 Windows 용 Sysprep 또는 Linux 용으로 적절 한 도구를 사용 하 여 일반화 된 운영 체제 이미지입니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-109">The image is a generalized operating system image, using either Sysprep for Windows or, for Linux, using the appropriate tool for the distribution.</span></span>

## <span data-ttu-id="2a9d1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2a9d1-110">EXAMPLES</span></span>

### <span data-ttu-id="2a9d1-111">예제 1: 리포지토리에 운영 체제 이미지 추가</span><span class="sxs-lookup"><span data-stu-id="2a9d1-111">Example 1: Add an operating system image to the repository</span></span>
```
PS C:\> $S = New-AzureVMImageDiskConfigSet
PS C:\> Set-AzureVMImageOSDiskConfig -DiskConfig $S -HostCaching ReadWrite -OSState "Generalized" -OS "Windows" -MediaLink $Link
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test1" -HostCaching ReadWrite -Lun 0 -MediaLink $Link1
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4" -HostCaching ReadWrite -Lun 0 -MediaLink $Link
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4"
PS C:\> $IMGName = "TestCREATEvmimage2";
PS C:\> Add-AzureVMImage -ImageName $IMGName -Label "Test1" -Description "Test1" -DiskConfig $S -Eula "http://www.contoso.com" -ImageFamily Windows -PublishedDate (Get-Date) -PrivacyUri "http://www.test.com" -RecommendedVMSize Small -IconName "Icon01" -SmallIconName "SmallIcon01" -ShowInGui
```

<span data-ttu-id="2a9d1-112">이 예제에서는 운영 체제 이미지를 리포지토리에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-112">This example adds an operating system image to the repository.</span></span>

## <span data-ttu-id="2a9d1-113">변수</span><span class="sxs-lookup"><span data-stu-id="2a9d1-113">PARAMETERS</span></span>

### <span data-ttu-id="2a9d1-114">-설명</span><span class="sxs-lookup"><span data-stu-id="2a9d1-114">-Description</span></span>
<span data-ttu-id="2a9d1-115">운영 체제 이미지에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-115">Specifies the description of the operating system image.</span></span>

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

### <span data-ttu-id="2a9d1-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="2a9d1-116">-DiskConfig</span></span>
<span data-ttu-id="2a9d1-117">가상 컴퓨터 이미지의 운영 체제 디스크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-117">Specifies the operating system disk configuration for the virtual machine image.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: VMImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-118">-Eula</span><span class="sxs-lookup"><span data-stu-id="2a9d1-118">-Eula</span></span>
<span data-ttu-id="2a9d1-119">최종 사용자 사용권 계약을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-119">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="2a9d1-120">이 값에 대 한 URL을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-120">It is recommended that you use an URL for this value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-121">-IconName</span><span class="sxs-lookup"><span data-stu-id="2a9d1-121">-IconName</span></span>
<span data-ttu-id="2a9d1-122">이미지를 리포지토리에 추가할 때 사용 되는 아이콘의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-122">Specifies the name of the icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-123">-Image\img패밀리</span><span class="sxs-lookup"><span data-stu-id="2a9d1-123">-ImageFamily</span></span>
<span data-ttu-id="2a9d1-124">운영 체제 이미지를 그룹화 하는 데 사용 되는 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-124">Specifies a value that is used to group operating system images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-125">-ImageName</span><span class="sxs-lookup"><span data-stu-id="2a9d1-125">-ImageName</span></span>
<span data-ttu-id="2a9d1-126">이미지 리포지토리에 추가 되는 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-126">Specifies the name of the image being added to the image repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2a9d1-127">-InformationAction</span></span>
<span data-ttu-id="2a9d1-128">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2a9d1-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a9d1-130">하기로</span><span class="sxs-lookup"><span data-stu-id="2a9d1-130">Continue</span></span>
- <span data-ttu-id="2a9d1-131">숨기기</span><span class="sxs-lookup"><span data-stu-id="2a9d1-131">Ignore</span></span>
- <span data-ttu-id="2a9d1-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="2a9d1-132">Inquire</span></span>
- <span data-ttu-id="2a9d1-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2a9d1-133">SilentlyContinue</span></span>
- <span data-ttu-id="2a9d1-134">중지가</span><span class="sxs-lookup"><span data-stu-id="2a9d1-134">Stop</span></span>
- <span data-ttu-id="2a9d1-135">대기</span><span class="sxs-lookup"><span data-stu-id="2a9d1-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2a9d1-136">-InformationVariable</span></span>
<span data-ttu-id="2a9d1-137">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-138">-레이블</span><span class="sxs-lookup"><span data-stu-id="2a9d1-138">-Label</span></span>
<span data-ttu-id="2a9d1-139">이미지에 지정할 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-139">Specifies a label to give the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-140">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="2a9d1-140">-MediaLocation</span></span>
<span data-ttu-id="2a9d1-141">이미지가 있는 실제 blob 페이지의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-141">Specifies the location of the physical blob page where the image resides.</span></span>
<span data-ttu-id="2a9d1-142">현재 구독 저장소의 blob 페이지에 대 한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-142">This is a link to a blob page in the current subscription's storage.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-143">-OS</span><span class="sxs-lookup"><span data-stu-id="2a9d1-143">-OS</span></span>
<span data-ttu-id="2a9d1-144">이미지의 운영 체제 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-144">Specifies the operating system version of the image.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: VMImage
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-145">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="2a9d1-145">-PrivacyUri</span></span>
<span data-ttu-id="2a9d1-146">운영 체제 이미지와 관련 된 개인 정보 정책이 포함 된 문서를 가리키는 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-146">Specifies the URL that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-147">-프로필</span><span class="sxs-lookup"><span data-stu-id="2a9d1-147">-Profile</span></span>
<span data-ttu-id="2a9d1-148">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2a9d1-149">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2a9d1-150">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="2a9d1-150">-PublishedDate</span></span>
<span data-ttu-id="2a9d1-151">운영 체제 이미지가 이미지 리포지토리에 추가 된 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-151">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-152">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="2a9d1-152">-RecommendedVMSize</span></span>
<span data-ttu-id="2a9d1-153">운영 체제 이미지에서 만든 가상 컴퓨터에 사용할 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-153">Specifies the size to use for the virtual machine that is created from the operating system image.</span></span>

<span data-ttu-id="2a9d1-154">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a9d1-155">높음이나</span><span class="sxs-lookup"><span data-stu-id="2a9d1-155">Medium</span></span>
- <span data-ttu-id="2a9d1-156">용량의</span><span class="sxs-lookup"><span data-stu-id="2a9d1-156">Large</span></span>
- <span data-ttu-id="2a9d1-157">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="2a9d1-157">ExtraLarge</span></span>
- <span data-ttu-id="2a9d1-158">5</span><span class="sxs-lookup"><span data-stu-id="2a9d1-158">A5</span></span>
- <span data-ttu-id="2a9d1-159">A6</span><span class="sxs-lookup"><span data-stu-id="2a9d1-159">A6</span></span>
- <span data-ttu-id="2a9d1-160">(A</span><span class="sxs-lookup"><span data-stu-id="2a9d1-160">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-161">-ShowInGui</span><span class="sxs-lookup"><span data-stu-id="2a9d1-161">-ShowInGui</span></span>
<span data-ttu-id="2a9d1-162">이 cmdlet이 GUI의 이미지를 표시 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-162">Indicates that this cmdlet shows the image in the GUI.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-163">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="2a9d1-163">-SmallIconName</span></span>
<span data-ttu-id="2a9d1-164">이미지를 리포지토리에 추가할 때 사용 되는 작은 아이콘의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-164">Specifies the name of the small icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9d1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9d1-165">CommonParameters</span></span>
<span data-ttu-id="2a9d1-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a9d1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9d1-167">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a9d1-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9d1-168">입력</span><span class="sxs-lookup"><span data-stu-id="2a9d1-168">INPUTS</span></span>

## <span data-ttu-id="2a9d1-169">출력</span><span class="sxs-lookup"><span data-stu-id="2a9d1-169">OUTPUTS</span></span>

### <span data-ttu-id="2a9d1-170">O Agecontext</span><span class="sxs-lookup"><span data-stu-id="2a9d1-170">OSImageContext</span></span>

## <span data-ttu-id="2a9d1-171">상속자</span><span class="sxs-lookup"><span data-stu-id="2a9d1-171">NOTES</span></span>

## <span data-ttu-id="2a9d1-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a9d1-172">RELATED LINKS</span></span>

[<span data-ttu-id="2a9d1-173">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="2a9d1-173">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="2a9d1-174">제거-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="2a9d1-174">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="2a9d1-175">저장-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="2a9d1-175">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="2a9d1-176">업데이트-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="2a9d1-176">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


