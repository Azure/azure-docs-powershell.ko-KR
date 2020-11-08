---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045995"
---
# <span data-ttu-id="dded9-101">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="dded9-101">New-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="dded9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dded9-102">SYNOPSIS</span></span>
<span data-ttu-id="dded9-103">Azure RemoteApp 템플릿 이미지를 업로드 하거나 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-103">Uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="dded9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dded9-104">SYNTAX</span></span>

### <span data-ttu-id="dded9-105">UploadLocalVhd (기본값)</span><span class="sxs-lookup"><span data-stu-id="dded9-105">UploadLocalVhd (Default)</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="dded9-106">AzureVmUpload</span><span class="sxs-lookup"><span data-stu-id="dded9-106">AzureVmUpload</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dded9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dded9-107">DESCRIPTION</span></span>
<span data-ttu-id="dded9-108">**AzureRemoteAppTemplateImage** Cmdlet은 Azure RemoteApp 템플릿 이미지를 업로드 하거나 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-108">The **New-AzureRemoteAppTemplateImage** cmdlet uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="dded9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dded9-109">EXAMPLES</span></span>

### <span data-ttu-id="dded9-110">예제 1: VHD 파일을 업로드 하 여 템플릿 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="dded9-110">Example 1: Upload a VHD file to create a template image</span></span>
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

<span data-ttu-id="dded9-111">이 명령은 C:\RemoteAppImages\ContosoApps.vhd를 업로드 하 여 북부 유럽 데이터 센터의 ContosoApps 이라는 서식 파일 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-111">This command uploads C:\RemoteAppImages\ContosoApps.vhd to create a template image named ContosoApps in the North Europe data center.</span></span>

## <span data-ttu-id="dded9-112">변수</span><span class="sxs-lookup"><span data-stu-id="dded9-112">PARAMETERS</span></span>

### <span data-ttu-id="dded9-113">-AzureVmImageName</span><span class="sxs-lookup"><span data-stu-id="dded9-113">-AzureVmImageName</span></span>
<span data-ttu-id="dded9-114">템플릿 이미지로 사용할 Azure 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-114">Specifies the name of an Azure virtual machine to use as a template image.</span></span>

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dded9-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="dded9-115">-ImageName</span></span>
<span data-ttu-id="dded9-116">Azure RemoteApp 템플릿 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dded9-117">-위치</span><span class="sxs-lookup"><span data-stu-id="dded9-117">-Location</span></span>
<span data-ttu-id="dded9-118">서식 파일 이미지의 Azure 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-118">Specifies the Azure region of the template image.</span></span>

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

### <span data-ttu-id="dded9-119">-Path</span><span class="sxs-lookup"><span data-stu-id="dded9-119">-Path</span></span>
<span data-ttu-id="dded9-120">서식 파일 이미지의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-120">Specifies the file path of the template image.</span></span>

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dded9-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="dded9-121">-Profile</span></span>
<span data-ttu-id="dded9-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dded9-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dded9-124">-Resume</span><span class="sxs-lookup"><span data-stu-id="dded9-124">-Resume</span></span>
<span data-ttu-id="dded9-125">서식 파일 이미지 업로드가 중단 된 경우이 cmdlet이 다시 시작 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-125">Indicates that this cmdlet resumes if the upload of a template image is interrupted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dded9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dded9-126">CommonParameters</span></span>
<span data-ttu-id="dded9-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dded9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dded9-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dded9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dded9-129">입력</span><span class="sxs-lookup"><span data-stu-id="dded9-129">INPUTS</span></span>

## <span data-ttu-id="dded9-130">출력</span><span class="sxs-lookup"><span data-stu-id="dded9-130">OUTPUTS</span></span>

## <span data-ttu-id="dded9-131">상속자</span><span class="sxs-lookup"><span data-stu-id="dded9-131">NOTES</span></span>

## <span data-ttu-id="dded9-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dded9-132">RELATED LINKS</span></span>

[<span data-ttu-id="dded9-133">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="dded9-133">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="dded9-134">제거-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="dded9-134">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="dded9-135">이름 바꾸기-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="dded9-135">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


