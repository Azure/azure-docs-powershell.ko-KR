---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 636280D6-32C3-48EF-A271-A4E032F8B334
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0dab3720a4680805e16f695a1ab1b2350554e8f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046319"
---
# <span data-ttu-id="696fc-101">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="696fc-101">Get-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="696fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696fc-102">SYNOPSIS</span></span>
<span data-ttu-id="696fc-103">컬렉션에 대해 게시 된 하나 이상의 Azure RemoteApp 프로그램의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="696fc-103">Retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="696fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="696fc-104">SYNTAX</span></span>

### <span data-ttu-id="696fc-105">FilterByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="696fc-105">FilterByName (Default)</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-RemoteAppProgram] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="696fc-106">FilterByAlias</span><span class="sxs-lookup"><span data-stu-id="696fc-106">FilterByAlias</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="696fc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="696fc-107">DESCRIPTION</span></span>
<span data-ttu-id="696fc-108">**AzureRemoteAppProgram** cmdlet은 컬렉션에 대해 게시 된 하나 이상의 Azure RemoteApp 프로그램의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="696fc-108">The **Get-AzureRemoteAppProgram** cmdlet retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="696fc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="696fc-109">EXAMPLES</span></span>

### <span data-ttu-id="696fc-110">예제 1: 프로그램의 속성 검색</span><span class="sxs-lookup"><span data-stu-id="696fc-110">Example 1: Retrieve the properties of a program</span></span>
```
PS C:\> Get-AzureRemoteAppProgram -CollectionName "ContosoApps" -RemoteAppProgram "Finance App"

Alias                : edc85816-4b9e-4284-b3dc-faedb505f5d9

AvailableToUsers     : True

CommandLineArguments : 

IconPngUris          : Microsoft.Azure.Management.RemoteApp.Models.IconPngUrisType

IconUri              : https://liverdcxstorage.blob.core.windows.net/icons/12345678-1234-1234-1234-123412341234.ico?se=2015-03-01T17%3A29%3A51Z&amp;amp;sr=b&amp;amp;sp=r&amp;amp;sig=abcdCCavbcF%2asY4RascaBauishCasd2FasdBHtasd2BPasdi5dasdD

Name                 : Contoso Finance

Status               : Published

VirtualPath          : %SYSTEMDRIVE%\Program Files (x86)\Contoso Finance\Finance.exe
```

<span data-ttu-id="696fc-111">이 명령은 Azure RemoteApp 프로그램의 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="696fc-111">This command displays the properties of an Azure RemoteApp program.</span></span>
<span data-ttu-id="696fc-112">재무 앱 이라는 프로그램은 ContosoApps 이라는 Azure RemoteApp 컬렉션에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="696fc-112">The program, named Finance App, is in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="696fc-113">변수</span><span class="sxs-lookup"><span data-stu-id="696fc-113">PARAMETERS</span></span>

### <span data-ttu-id="696fc-114">-별칭</span><span class="sxs-lookup"><span data-stu-id="696fc-114">-Alias</span></span>
<span data-ttu-id="696fc-115">속성을 검색할 프로그램의 별칭을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696fc-115">Specifies the alias of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByAlias
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696fc-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="696fc-116">-CollectionName</span></span>
<span data-ttu-id="696fc-117">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696fc-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="696fc-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="696fc-118">-Profile</span></span>
<span data-ttu-id="696fc-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696fc-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="696fc-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="696fc-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="696fc-121">-RemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="696fc-121">-RemoteAppProgram</span></span>
<span data-ttu-id="696fc-122">속성을 검색할 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696fc-122">Specifies the name of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="696fc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696fc-123">CommonParameters</span></span>
<span data-ttu-id="696fc-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="696fc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696fc-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="696fc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696fc-126">입력</span><span class="sxs-lookup"><span data-stu-id="696fc-126">INPUTS</span></span>

## <span data-ttu-id="696fc-127">출력</span><span class="sxs-lookup"><span data-stu-id="696fc-127">OUTPUTS</span></span>

## <span data-ttu-id="696fc-128">상속자</span><span class="sxs-lookup"><span data-stu-id="696fc-128">NOTES</span></span>

## <span data-ttu-id="696fc-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="696fc-129">RELATED LINKS</span></span>

[<span data-ttu-id="696fc-130">게시-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="696fc-130">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)

[<span data-ttu-id="696fc-131">게시 취소-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="696fc-131">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


