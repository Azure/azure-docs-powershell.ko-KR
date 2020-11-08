---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045474"
---
# <span data-ttu-id="e7d51-101">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e7d51-101">Rename-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="e7d51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d51-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d51-103">Azure RemoteApp 템플릿 이미지의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="e7d51-103">Renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="e7d51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7d51-104">SYNTAX</span></span>

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7d51-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e7d51-105">DESCRIPTION</span></span>
<span data-ttu-id="e7d51-106">**AzureRemoteAppTemplateImage** Cmdlet은 Azure RemoteApp 템플릿 이미지의 이름을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d51-106">The **Rename-AzureRemoteAppTemplateImage** cmdlet renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="e7d51-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e7d51-107">EXAMPLES</span></span>

### <span data-ttu-id="e7d51-108">예제 1: 서식 파일 이미지 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="e7d51-108">Example 1: Rename a template image</span></span>
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

<span data-ttu-id="e7d51-109">이 명령은 ContosoApps 이라는 Azure RemoteApp 템플릿 이미지의 이름을 ContosoFinanceApps로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="e7d51-109">This command renames the Azure RemoteApp template image named ContosoApps to ContosoFinanceApps.</span></span>

## <span data-ttu-id="e7d51-110">변수</span><span class="sxs-lookup"><span data-stu-id="e7d51-110">PARAMETERS</span></span>

### <span data-ttu-id="e7d51-111">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e7d51-111">-ImageName</span></span>
<span data-ttu-id="e7d51-112">이름을 바꿀 Azure RemoteApp 템플릿 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d51-112">Specifies the name of an Azure RemoteApp template image to rename.</span></span>

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

### <span data-ttu-id="e7d51-113">-NewName</span><span class="sxs-lookup"><span data-stu-id="e7d51-113">-NewName</span></span>
<span data-ttu-id="e7d51-114">Azure RemoteApp 템플릿 이미지의 새 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d51-114">Specifies a new name for an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d51-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="e7d51-115">-Profile</span></span>
<span data-ttu-id="e7d51-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d51-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7d51-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d51-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7d51-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d51-118">CommonParameters</span></span>
<span data-ttu-id="e7d51-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d51-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d51-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7d51-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d51-121">입력</span><span class="sxs-lookup"><span data-stu-id="e7d51-121">INPUTS</span></span>

## <span data-ttu-id="e7d51-122">출력</span><span class="sxs-lookup"><span data-stu-id="e7d51-122">OUTPUTS</span></span>

## <span data-ttu-id="e7d51-123">상속자</span><span class="sxs-lookup"><span data-stu-id="e7d51-123">NOTES</span></span>

## <span data-ttu-id="e7d51-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7d51-124">RELATED LINKS</span></span>

[<span data-ttu-id="e7d51-125">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e7d51-125">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="e7d51-126">새로운 AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e7d51-126">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="e7d51-127">제거-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e7d51-127">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)


