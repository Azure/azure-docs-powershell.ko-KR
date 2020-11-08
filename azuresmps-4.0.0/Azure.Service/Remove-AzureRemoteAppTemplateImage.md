---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046149"
---
# <span data-ttu-id="63856-101">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="63856-101">Remove-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="63856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63856-102">SYNOPSIS</span></span>
<span data-ttu-id="63856-103">Azure RemoteApp 템플릿 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="63856-103">Deletes an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="63856-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63856-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63856-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63856-105">DESCRIPTION</span></span>
<span data-ttu-id="63856-106">**AzureRemoteAppTemplateImage** Cmdlet은 Azure RemoteApp 템플릿 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="63856-106">The **Remove-AzureRemoteAppTemplateImage** cmdlet deletes an Azure RemoteApp template image.</span></span>
<span data-ttu-id="63856-107">템플릿 이미지는 Azure RemoteApp 컬렉션에 연결 되지 않은 경우에만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63856-107">A template image can deleted only if it is not linked to any Azure RemoteApp collection.</span></span>

## <span data-ttu-id="63856-108">예제의</span><span class="sxs-lookup"><span data-stu-id="63856-108">EXAMPLES</span></span>

### <span data-ttu-id="63856-109">예제 1: 서식 파일 이미지 삭제</span><span class="sxs-lookup"><span data-stu-id="63856-109">Example 1: Delete a template image</span></span>
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="63856-110">이 명령은 ContosoApps 이라는 서식 파일 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="63856-110">This command deletes the template image named ContosoApps.</span></span>

## <span data-ttu-id="63856-111">변수</span><span class="sxs-lookup"><span data-stu-id="63856-111">PARAMETERS</span></span>

### <span data-ttu-id="63856-112">-ImageName</span><span class="sxs-lookup"><span data-stu-id="63856-112">-ImageName</span></span>
<span data-ttu-id="63856-113">RemoteApp 템플릿 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63856-113">Specifies the name of the RemoteApp template image.</span></span>

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

### <span data-ttu-id="63856-114">-프로필</span><span class="sxs-lookup"><span data-stu-id="63856-114">-Profile</span></span>
<span data-ttu-id="63856-115">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63856-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="63856-116">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="63856-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="63856-117">-확인</span><span class="sxs-lookup"><span data-stu-id="63856-117">-Confirm</span></span>
<span data-ttu-id="63856-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63856-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63856-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63856-119">-WhatIf</span></span>
<span data-ttu-id="63856-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63856-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63856-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63856-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63856-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63856-122">CommonParameters</span></span>
<span data-ttu-id="63856-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63856-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63856-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63856-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63856-125">입력</span><span class="sxs-lookup"><span data-stu-id="63856-125">INPUTS</span></span>

## <span data-ttu-id="63856-126">출력</span><span class="sxs-lookup"><span data-stu-id="63856-126">OUTPUTS</span></span>

## <span data-ttu-id="63856-127">상속자</span><span class="sxs-lookup"><span data-stu-id="63856-127">NOTES</span></span>

## <span data-ttu-id="63856-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63856-128">RELATED LINKS</span></span>

[<span data-ttu-id="63856-129">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="63856-129">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="63856-130">새로운 AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="63856-130">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="63856-131">이름 바꾸기-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="63856-131">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


