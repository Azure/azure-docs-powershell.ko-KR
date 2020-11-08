---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046583"
---
# <span data-ttu-id="ae183-101">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ae183-101">Update-AzureVMImage</span></span>

## <span data-ttu-id="ae183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae183-102">SYNOPSIS</span></span>
<span data-ttu-id="ae183-103">이미지 리포지토리에서 운영 체제 이미지의 레이블을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-103">Updates the label of an operating system image in the image repository.</span></span>

## <span data-ttu-id="ae183-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae183-104">SYNTAX</span></span>

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ae183-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae183-105">DESCRIPTION</span></span>
<span data-ttu-id="ae183-106">**업데이트-AzureVMImage** cmdlet은 이미지 리포지토리의 운영 체제 이미지에서 레이블을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-106">The **Update-AzureVMImage** cmdlet updates the label on an operating system image in the image repository.</span></span>
<span data-ttu-id="ae183-107">업데이트 된 이미지에 대 한 정보가 포함 된 image 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-107">It returns an image object with information about the updated image.</span></span>

## <span data-ttu-id="ae183-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ae183-108">EXAMPLES</span></span>

### <span data-ttu-id="ae183-109">예제 1: 이미지 레이블을 변경 하 여 이미지 업데이트</span><span class="sxs-lookup"><span data-stu-id="ae183-109">Example 1: Update an image by changing the image label</span></span>
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

<span data-ttu-id="ae183-110">이 명령은 이미지 레이블을 DoNotUse로 변경 하 여 Windows-서버-2008-SP2의 이미지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-110">This command updates the image named Windows-Server-2008-SP2 by changing the image label to DoNotUse.</span></span>

### <span data-ttu-id="ae183-111">예제 2: 레이블로 모든 운영 체제 가져오기 후 레이블 업데이트</span><span class="sxs-lookup"><span data-stu-id="ae183-111">Example 2: Get all operating systems by label and then update the label</span></span>
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

<span data-ttu-id="ae183-112">이 명령은 DoNotUse 라는 레이블이 지정 된 모든 운영 체제 이미지를 가져오고 레이블을 업데이트 됨으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-112">This command gets all the operating system images labeled DoNotUse and changes the label to Updated.</span></span>

## <span data-ttu-id="ae183-113">변수</span><span class="sxs-lookup"><span data-stu-id="ae183-113">PARAMETERS</span></span>

### <span data-ttu-id="ae183-114">-설명</span><span class="sxs-lookup"><span data-stu-id="ae183-114">-Description</span></span>
<span data-ttu-id="ae183-115">운영 체제 이미지에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-115">Specifies the description of the operating system image.</span></span>

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

### <span data-ttu-id="ae183-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="ae183-116">-DiskConfig</span></span>
<span data-ttu-id="ae183-117">**AzureVMImageDiskConfigSet** , **AzureVMImageOSDiskConfig** 및 **set AzureVMImageDataDiskConfig** cmdlet을 사용 하 여 만든 가상 컴퓨터 이미지에 대 한 운영 체제 디스크 및 데이터 디스크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-117">Specifies the operating system disk and data disk configuration for the virtual machine image created by using the **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** , and **Set-AzureVMImageDataDiskConfig** cmdlets.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae183-118">-DontShowInGui</span><span class="sxs-lookup"><span data-stu-id="ae183-118">-DontShowInGui</span></span>
<span data-ttu-id="ae183-119">이 cmdlet이 GUI에서 이미지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-119">Indicates that this cmdlet does not show the image in the GUI.</span></span>

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

### <span data-ttu-id="ae183-120">-Eula</span><span class="sxs-lookup"><span data-stu-id="ae183-120">-Eula</span></span>
<span data-ttu-id="ae183-121">최종 사용자 사용권 계약을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-121">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="ae183-122">값을 URL로 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-122">We recommend that the value is a URL.</span></span>

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

### <span data-ttu-id="ae183-123">-IconName</span><span class="sxs-lookup"><span data-stu-id="ae183-123">-IconName</span></span>
<span data-ttu-id="ae183-124">운영 체제 또는 가상 컴퓨터 이미지의 표준 아이콘 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-124">Specifies the standard icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="ae183-125">-Image\img패밀리</span><span class="sxs-lookup"><span data-stu-id="ae183-125">-ImageFamily</span></span>
<span data-ttu-id="ae183-126">운영 체제 또는 가상 컴퓨터 이미지를 그룹화 하는 데 사용할 수 있는 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-126">Specifies a value that can be used to group operating system or virtual machine images.</span></span>

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

### <span data-ttu-id="ae183-127">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ae183-127">-ImageName</span></span>
<span data-ttu-id="ae183-128">이미지 리포지토리에서 업데이트할 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-128">Specifies the name of the image to update in the image repository.</span></span>

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

### <span data-ttu-id="ae183-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ae183-129">-InformationAction</span></span>
<span data-ttu-id="ae183-130">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ae183-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae183-132">하기로</span><span class="sxs-lookup"><span data-stu-id="ae183-132">Continue</span></span>
- <span data-ttu-id="ae183-133">숨기기</span><span class="sxs-lookup"><span data-stu-id="ae183-133">Ignore</span></span>
- <span data-ttu-id="ae183-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="ae183-134">Inquire</span></span>
- <span data-ttu-id="ae183-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ae183-135">SilentlyContinue</span></span>
- <span data-ttu-id="ae183-136">중지가</span><span class="sxs-lookup"><span data-stu-id="ae183-136">Stop</span></span>
- <span data-ttu-id="ae183-137">대기</span><span class="sxs-lookup"><span data-stu-id="ae183-137">Suspend</span></span>

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

### <span data-ttu-id="ae183-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ae183-138">-InformationVariable</span></span>
<span data-ttu-id="ae183-139">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ae183-140">-레이블</span><span class="sxs-lookup"><span data-stu-id="ae183-140">-Label</span></span>
<span data-ttu-id="ae183-141">이미지의 새 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-141">Specifies the new label of the image.</span></span>

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

### <span data-ttu-id="ae183-142">-언어</span><span class="sxs-lookup"><span data-stu-id="ae183-142">-Language</span></span>
<span data-ttu-id="ae183-143">가상 머신 또는 운영 체제 이미지의 운영 체제에 대 한 언어를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-143">Specifies the language for the operating system in the virtual machine or operating system image.</span></span>

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

### <span data-ttu-id="ae183-144">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="ae183-144">-PrivacyUri</span></span>
<span data-ttu-id="ae183-145">운영 체제 이미지와 관련 된 개인 정보 정책이 포함 된 문서를 가리키는 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-145">Specifies the URI that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae183-146">-프로필</span><span class="sxs-lookup"><span data-stu-id="ae183-146">-Profile</span></span>
<span data-ttu-id="ae183-147">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae183-148">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae183-149">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="ae183-149">-PublishedDate</span></span>
<span data-ttu-id="ae183-150">운영 체제 이미지가 이미지 리포지토리에 추가 된 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-150">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae183-151">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="ae183-151">-RecommendedVMSize</span></span>
<span data-ttu-id="ae183-152">가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-152">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="ae183-153">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae183-154">높음이나</span><span class="sxs-lookup"><span data-stu-id="ae183-154">Medium</span></span>
- <span data-ttu-id="ae183-155">용량의</span><span class="sxs-lookup"><span data-stu-id="ae183-155">Large</span></span>
- <span data-ttu-id="ae183-156">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="ae183-156">ExtraLarge</span></span>
- <span data-ttu-id="ae183-157">5</span><span class="sxs-lookup"><span data-stu-id="ae183-157">A5</span></span>
- <span data-ttu-id="ae183-158">A6</span><span class="sxs-lookup"><span data-stu-id="ae183-158">A6</span></span>
- <span data-ttu-id="ae183-159">(A</span><span class="sxs-lookup"><span data-stu-id="ae183-159">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae183-160">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="ae183-160">-SmallIconName</span></span>
<span data-ttu-id="ae183-161">운영 체제 또는 가상 컴퓨터 이미지의 작은 아이콘 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-161">Specifies the small icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="ae183-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae183-162">CommonParameters</span></span>
<span data-ttu-id="ae183-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae183-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae183-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae183-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae183-165">입력</span><span class="sxs-lookup"><span data-stu-id="ae183-165">INPUTS</span></span>

## <span data-ttu-id="ae183-166">출력</span><span class="sxs-lookup"><span data-stu-id="ae183-166">OUTPUTS</span></span>

### <span data-ttu-id="ae183-167">O Agecontext</span><span class="sxs-lookup"><span data-stu-id="ae183-167">OSImageContext</span></span>

## <span data-ttu-id="ae183-168">상속자</span><span class="sxs-lookup"><span data-stu-id="ae183-168">NOTES</span></span>

## <span data-ttu-id="ae183-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae183-169">RELATED LINKS</span></span>

[<span data-ttu-id="ae183-170">추가-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ae183-170">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="ae183-171">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ae183-171">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="ae183-172">제거-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ae183-172">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="ae183-173">저장-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ae183-173">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="ae183-174">새로운 AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="ae183-174">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="ae183-175">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ae183-175">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="ae183-176">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ae183-176">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


