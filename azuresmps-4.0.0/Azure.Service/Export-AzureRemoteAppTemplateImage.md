---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D35C580F-437A-40F9-B6BA-412A1176292A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9821602df196604100de5926a7d9510bdb011bd2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045681"
---
# <span data-ttu-id="b4555-101">Export-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b4555-101">Export-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="b4555-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4555-102">SYNOPSIS</span></span>
<span data-ttu-id="b4555-103">하나의 Azure RemoteApp 컬렉션의 템플릿 이미지를 지정 된 Azure 저장소 계정으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-103">Exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="b4555-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4555-104">SYNTAX</span></span>

```
Export-AzureRemoteAppTemplateImage [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingTemplateImage] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4555-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4555-105">DESCRIPTION</span></span>
<span data-ttu-id="b4555-106">**Export-AzureRemoteAppTemplateImage** cmdlet은 하나의 azure RemoteApp 컬렉션의 템플릿 이미지를 지정 된 azure 저장소 계정으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-106">The **Export-AzureRemoteAppTemplateImage** cmdlet exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="b4555-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b4555-107">EXAMPLES</span></span>

### <span data-ttu-id="b4555-108">예제 1: Azure 저장소 계정으로 서식 파일 이미지 내보내기</span><span class="sxs-lookup"><span data-stu-id="b4555-108">Example 1: Export a template image to the Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppTemplateImage -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingTemplateImage
```

<span data-ttu-id="b4555-109">이 명령은 Contoso 라는 컬렉션의 템플릿 이미지를 지정 된 Azure storage 계정에서 이름 AccountName 및 key AccountKey 인 ContainerName 이라는 컨테이너로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-109">This command exports the template image of the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="b4555-110">변수</span><span class="sxs-lookup"><span data-stu-id="b4555-110">PARAMETERS</span></span>

### <span data-ttu-id="b4555-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="b4555-111">-CollectionName</span></span>
<span data-ttu-id="b4555-112">원본 Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="b4555-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="b4555-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="b4555-114">대상 Azure 저장소 계정에서 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4555-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4555-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="b4555-116">대상 Azure 저장소 계정의 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-116">Specifies the key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4555-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4555-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="b4555-118">대상 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-118">Specifies the name of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="b4555-119">-OverwriteExistingTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b4555-119">-OverwriteExistingTemplateImage</span></span>
<span data-ttu-id="b4555-120">Cmdlet이 기존 템플릿 이미지를 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-120">Indicates that the cmdlet overwrites the existing template image.</span></span>

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

### <span data-ttu-id="b4555-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="b4555-121">-Profile</span></span>
<span data-ttu-id="b4555-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4555-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4555-124">-확인</span><span class="sxs-lookup"><span data-stu-id="b4555-124">-Confirm</span></span>
<span data-ttu-id="b4555-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4555-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4555-126">-WhatIf</span></span>
<span data-ttu-id="b4555-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4555-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4555-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4555-129">CommonParameters</span></span>
<span data-ttu-id="b4555-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4555-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4555-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4555-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4555-132">입력</span><span class="sxs-lookup"><span data-stu-id="b4555-132">INPUTS</span></span>

## <span data-ttu-id="b4555-133">출력</span><span class="sxs-lookup"><span data-stu-id="b4555-133">OUTPUTS</span></span>

## <span data-ttu-id="b4555-134">상속자</span><span class="sxs-lookup"><span data-stu-id="b4555-134">NOTES</span></span>

## <span data-ttu-id="b4555-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4555-135">RELATED LINKS</span></span>

[<span data-ttu-id="b4555-136">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b4555-136">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b4555-137">새로운 AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b4555-137">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b4555-138">제거-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b4555-138">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b4555-139">이름 바꾸기-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b4555-139">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


