---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045884"
---
# <span data-ttu-id="e4c46-101">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="e4c46-101">Publish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="e4c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4c46-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c46-103">Azure RemoteApp 프로그램을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-103">Publishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="e4c46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4c46-104">SYNTAX</span></span>

### <span data-ttu-id="e4c46-105">앱 Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="e4c46-105">App Id (Default)</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e4c46-106">앱 경로</span><span class="sxs-lookup"><span data-stu-id="e4c46-106">App Path</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e4c46-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e4c46-107">DESCRIPTION</span></span>
<span data-ttu-id="e4c46-108">**AzureRemoteAppProgram** cmdlet은 azure remoteapp 컬렉션의 사용자가 사용할 수 있도록 azure remoteapp 프로그램을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-108">The **Publish-AzureRemoteAppProgram** cmdlet publishes an Azure RemoteApp program, which makes it available to users of the Azure RemoteApp collection.</span></span>

## <span data-ttu-id="e4c46-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e4c46-109">EXAMPLES</span></span>

### <span data-ttu-id="e4c46-110">예제 1: 컬렉션에 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="e4c46-110">Example 1: Publish a program in a collection</span></span>
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

<span data-ttu-id="e4c46-111">이 명령은 지정 된 *Startmenuappid* 를 사용 하 여 ContosoApps 컬렉션의 프로그램을 게시 하 여 시작 메뉴에 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-111">This command publishes the program in the ContosoApps collection with the specified *StartMenuAppId* to add the program to the Start Menu.</span></span>
<span data-ttu-id="e4c46-112">게시 된 앱은 "재무 앱"의 표시 이름을 갖게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-112">The published app will have a display name of "Finance App".</span></span>

## <span data-ttu-id="e4c46-113">변수</span><span class="sxs-lookup"><span data-stu-id="e4c46-113">PARAMETERS</span></span>

### <span data-ttu-id="e4c46-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e4c46-114">-CollectionName</span></span>
<span data-ttu-id="e4c46-115">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-115">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4c46-116">-명령줄</span><span class="sxs-lookup"><span data-stu-id="e4c46-116">-CommandLine</span></span>
<span data-ttu-id="e4c46-117">이 cmdlet이 게시 하는 프로그램의 명령줄 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-117">Specifies command-line arguments for the program that this cmdlet publishes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c46-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e4c46-118">-DisplayName</span></span>
<span data-ttu-id="e4c46-119">사용자에 게 친숙 한 Azure RemoteApp 프로그램의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-119">Specifies the user-friendly display name of the Azure RemoteApp program.</span></span>
<span data-ttu-id="e4c46-120">사용자는이를 응용 프로그램의 이름으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-120">Users see this as the name of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c46-121">-FileVirtualPath</span><span class="sxs-lookup"><span data-stu-id="e4c46-121">-FileVirtualPath</span></span>
<span data-ttu-id="e4c46-122">프로그램의 템플릿 이미지 내에서 프로그램의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-122">Specifies the path of the program within the template image of the program.</span></span>

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c46-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="e4c46-123">-Profile</span></span>
<span data-ttu-id="e4c46-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4c46-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4c46-126">-StartMenuAppId</span><span class="sxs-lookup"><span data-stu-id="e4c46-126">-StartMenuAppId</span></span>
<span data-ttu-id="e4c46-127">이 cmdlet이 프로그램을 시작 메뉴에 추가 하는 데 사용 하는 GUID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-127">Specifies a GUID that this cmdlet uses to add the program to the Start Menu.</span></span>

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4c46-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c46-128">CommonParameters</span></span>
<span data-ttu-id="e4c46-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c46-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c46-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4c46-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c46-131">입력</span><span class="sxs-lookup"><span data-stu-id="e4c46-131">INPUTS</span></span>

## <span data-ttu-id="e4c46-132">출력</span><span class="sxs-lookup"><span data-stu-id="e4c46-132">OUTPUTS</span></span>

## <span data-ttu-id="e4c46-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e4c46-133">NOTES</span></span>

## <span data-ttu-id="e4c46-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4c46-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4c46-135">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="e4c46-135">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="e4c46-136">게시 취소-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="e4c46-136">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


