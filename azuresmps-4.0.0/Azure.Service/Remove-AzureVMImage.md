---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046454"
---
# <span data-ttu-id="a1ba0-101">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a1ba0-101">Remove-AzureVMImage</span></span>

## <span data-ttu-id="a1ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ba0-103">이미지 리포지토리에서 운영 체제 이미지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-103">Removes an operating system image from the image repository.</span></span>

## <span data-ttu-id="a1ba0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1ba0-104">SYNTAX</span></span>

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a1ba0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a1ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="a1ba0-106">**AzureVMImage** cmdlet은 이미지 리포지토리에서 운영 체제 이미지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-106">The **Remove-AzureVMImage** cmdlet removes an operating system image from the image repository.</span></span>
<span data-ttu-id="a1ba0-107">기본적으로이 cmdlet은 저장소 계정에서 연결 된 실제 이미지 blob을 삭제 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-107">By default, this cmdlet does not delete the associated physical image blob from the storage account.</span></span>
<span data-ttu-id="a1ba0-108">연결 된 VHD (가상 하드 드라이브)를 삭제 하려면 **Deletevhd** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-108">To delete the associated virtual hard drive (VHD), use the **DeleteVHD** parameter.</span></span>

## <span data-ttu-id="a1ba0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a1ba0-109">EXAMPLES</span></span>

### <span data-ttu-id="a1ba0-110">예제 1: 이미지 리포지토리에서 이미지 제거</span><span class="sxs-lookup"><span data-stu-id="a1ba0-110">Example 1: Remove an image from the image repository</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

<span data-ttu-id="a1ba0-111">이 명령은 이미지 리포지토리에서 Image001 이라는 이미지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-111">This command removes the image named Image001 from the image repository.</span></span>

### <span data-ttu-id="a1ba0-112">예제 2: 이미지 리포지토리에서 이미지를 제거 하 고 VHD도</span><span class="sxs-lookup"><span data-stu-id="a1ba0-112">Example 2: Remove an image from the image repository and also the VHD</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

<span data-ttu-id="a1ba0-113">이 명령은 이미지 리포지토리에서 Image001 이라는 이미지를 제거 하 고 저장소 계정에서 실제 VHD 이미지도 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-113">This command removes the image named Image001 from the image repository and also deletes the physical VHD image from the storage account.</span></span>

### <span data-ttu-id="a1ba0-114">예제 3: 구독 컨텍스트를 설정한 다음 모든 이미지 제거</span><span class="sxs-lookup"><span data-stu-id="a1ba0-114">Example 3: Set a subscription context and then remove all the images</span></span>
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

<span data-ttu-id="a1ba0-115">이 명령은 구독 컨텍스트를 설정한 다음 해당 레이블에 이름 Beta가 포함 된 이미지 리포지토리에서 모든 이미지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-115">This command sets the subscription context and then removes all the images from the image repository whose Label includes the name Beta.</span></span>

## <span data-ttu-id="a1ba0-116">변수</span><span class="sxs-lookup"><span data-stu-id="a1ba0-116">PARAMETERS</span></span>

### <span data-ttu-id="a1ba0-117">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="a1ba0-117">-DeleteVHD</span></span>
<span data-ttu-id="a1ba0-118">이 cmdlet이 저장소 계정에서 실제 VHD 이미지 blob을 삭제 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-118">Indicates that this cmdlet deletes the physical VHD image blob from the storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1ba0-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a1ba0-119">-ImageName</span></span>
<span data-ttu-id="a1ba0-120">이미지 리포지토리에서 제거할 운영 체제 또는 가상 컴퓨터 이미지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-120">Specifies the operating system or virtual machine image to remove from the image repository.</span></span>

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

### <span data-ttu-id="a1ba0-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a1ba0-121">-InformationAction</span></span>
<span data-ttu-id="a1ba0-122">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a1ba0-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1ba0-124">하기로</span><span class="sxs-lookup"><span data-stu-id="a1ba0-124">Continue</span></span>
- <span data-ttu-id="a1ba0-125">숨기기</span><span class="sxs-lookup"><span data-stu-id="a1ba0-125">Ignore</span></span>
- <span data-ttu-id="a1ba0-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="a1ba0-126">Inquire</span></span>
- <span data-ttu-id="a1ba0-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a1ba0-127">SilentlyContinue</span></span>
- <span data-ttu-id="a1ba0-128">중지가</span><span class="sxs-lookup"><span data-stu-id="a1ba0-128">Stop</span></span>
- <span data-ttu-id="a1ba0-129">대기</span><span class="sxs-lookup"><span data-stu-id="a1ba0-129">Suspend</span></span>

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

### <span data-ttu-id="a1ba0-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a1ba0-130">-InformationVariable</span></span>
<span data-ttu-id="a1ba0-131">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a1ba0-132">-프로필</span><span class="sxs-lookup"><span data-stu-id="a1ba0-132">-Profile</span></span>
<span data-ttu-id="a1ba0-133">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1ba0-134">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1ba0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ba0-135">CommonParameters</span></span>
<span data-ttu-id="a1ba0-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ba0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ba0-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1ba0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ba0-138">입력</span><span class="sxs-lookup"><span data-stu-id="a1ba0-138">INPUTS</span></span>

## <span data-ttu-id="a1ba0-139">출력</span><span class="sxs-lookup"><span data-stu-id="a1ba0-139">OUTPUTS</span></span>

## <span data-ttu-id="a1ba0-140">상속자</span><span class="sxs-lookup"><span data-stu-id="a1ba0-140">NOTES</span></span>

## <span data-ttu-id="a1ba0-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1ba0-141">RELATED LINKS</span></span>

[<span data-ttu-id="a1ba0-142">추가-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a1ba0-142">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="a1ba0-143">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a1ba0-143">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="a1ba0-144">저장-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a1ba0-144">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="a1ba0-145">업데이트-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a1ba0-145">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


