---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046579"
---
# <span data-ttu-id="c38d3-101">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="c38d3-101">Get-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="c38d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c38d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c38d3-103">Azure RemoteApp 템플릿 이미지에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c38d3-103">Retrieves information about Azure RemoteApp template images.</span></span>

## <span data-ttu-id="c38d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c38d3-104">SYNTAX</span></span>

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c38d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c38d3-105">DESCRIPTION</span></span>
<span data-ttu-id="c38d3-106">**AzureRemoteAppTemplateImage** Cmdlet은 Microsoft Azure의 Azure RemoteApp 템플릿 이미지에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c38d3-106">The **Get-AzureRemoteAppTemplateImage** cmdlet retrieves information about Azure RemoteApp template images in Microsoft Azure.</span></span>
<span data-ttu-id="c38d3-107">이 cmdlet은 지정 된 템플릿 이미지에 대 한 정보를 포함 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c38d3-107">This cmdlet returns an object containing information about a specified template image.</span></span>
<span data-ttu-id="c38d3-108">서식 파일 이미지를 지정 하지 않으면 현재 구독에 있는 모든 템플릿 이미지에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c38d3-108">If no template image is specified, it retrieves information about all the template images in the current subscription.</span></span>

## <span data-ttu-id="c38d3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c38d3-109">EXAMPLES</span></span>

### <span data-ttu-id="c38d3-110">예제 1: 모든 템플릿 이미지 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="c38d3-110">Example 1: Get a list of all template images</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

<span data-ttu-id="c38d3-111">이 명령은 모든 템플릿 이미지 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c38d3-111">This command returns the list of all template images.</span></span>

### <span data-ttu-id="c38d3-112">예제 2: 지정 된 서식 파일 이미지에 대 한 정보 검색</span><span class="sxs-lookup"><span data-stu-id="c38d3-112">Example 2: Retrieve information about a specified template image</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="c38d3-113">이 명령은 ContosoApps 이라는 서식 파일 이미지에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c38d3-113">This command retrieves information about the template image named ContosoApps.</span></span>

## <span data-ttu-id="c38d3-114">변수</span><span class="sxs-lookup"><span data-stu-id="c38d3-114">PARAMETERS</span></span>

### <span data-ttu-id="c38d3-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="c38d3-115">-ImageName</span></span>
<span data-ttu-id="c38d3-116">Azure RemoteApp 템플릿 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c38d3-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="c38d3-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="c38d3-117">-Profile</span></span>
<span data-ttu-id="c38d3-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c38d3-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c38d3-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c38d3-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c38d3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38d3-120">CommonParameters</span></span>
<span data-ttu-id="c38d3-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c38d3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38d3-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c38d3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38d3-123">입력</span><span class="sxs-lookup"><span data-stu-id="c38d3-123">INPUTS</span></span>

## <span data-ttu-id="c38d3-124">출력</span><span class="sxs-lookup"><span data-stu-id="c38d3-124">OUTPUTS</span></span>

## <span data-ttu-id="c38d3-125">상속자</span><span class="sxs-lookup"><span data-stu-id="c38d3-125">NOTES</span></span>

## <span data-ttu-id="c38d3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c38d3-126">RELATED LINKS</span></span>

[<span data-ttu-id="c38d3-127">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c38d3-127">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="c38d3-128">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="c38d3-128">Get-AzureRemoteAppStartMenuProgram</span></span>](./Get-AzureRemoteAppStartMenuProgram.md)


