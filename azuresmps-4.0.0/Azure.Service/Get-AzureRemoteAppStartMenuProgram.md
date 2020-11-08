---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: FCDEA955-EB64-4EEA-9F4A-04E2C1F0A831
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83664e8be9241782e42d7ba7634691668ed575f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046315"
---
# <span data-ttu-id="ad59c-101">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="ad59c-101">Get-AzureRemoteAppStartMenuProgram</span></span>

## <span data-ttu-id="ad59c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad59c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad59c-103">Azure RemoteApp 컬렉션에 있는 시작 메뉴 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad59c-103">Lists the Start Menu programs in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="ad59c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad59c-104">SYNTAX</span></span>

```
Get-AzureRemoteAppStartMenuProgram [-CollectionName] <String> [[-ProgramName] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ad59c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad59c-105">DESCRIPTION</span></span>
<span data-ttu-id="ad59c-106">**AzureRemoteAppStartMenuProgram** Cmdlet은 Azure RemoteApp 컬렉션에서 사용 하는 서식 파일 이미지의 시작 메뉴 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad59c-106">The **Get-AzureRemoteAppStartMenuProgram** cmdlet lists the Start Menu programs in the template image that an Azure RemoteApp collection uses.</span></span>

## <span data-ttu-id="ad59c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ad59c-107">EXAMPLES</span></span>

### <span data-ttu-id="ad59c-108">예제 1: 컬렉션에 대 한 시작 메뉴 프로그램 나열</span><span class="sxs-lookup"><span data-stu-id="ad59c-108">Example 1: List the Start Menu programs for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppStartMenuProgram -CollectionName "ContosoApps"
```

<span data-ttu-id="ad59c-109">이 명령은 ContosoApps 컬렉션에 대 한 시작 메뉴 프로그램 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad59c-109">This command returns the list of Start Menu programs for the ContosoApps collection.</span></span>

## <span data-ttu-id="ad59c-110">변수</span><span class="sxs-lookup"><span data-stu-id="ad59c-110">PARAMETERS</span></span>

### <span data-ttu-id="ad59c-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="ad59c-111">-CollectionName</span></span>
<span data-ttu-id="ad59c-112">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad59c-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="ad59c-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="ad59c-113">-Profile</span></span>
<span data-ttu-id="ad59c-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad59c-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad59c-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ad59c-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ad59c-116">-ProgramName</span><span class="sxs-lookup"><span data-stu-id="ad59c-116">-ProgramName</span></span>
<span data-ttu-id="ad59c-117">정보를 나열할 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad59c-117">Specifies the name of a program for which to list information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ad59c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad59c-118">CommonParameters</span></span>
<span data-ttu-id="ad59c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad59c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad59c-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad59c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad59c-121">입력</span><span class="sxs-lookup"><span data-stu-id="ad59c-121">INPUTS</span></span>

## <span data-ttu-id="ad59c-122">출력</span><span class="sxs-lookup"><span data-stu-id="ad59c-122">OUTPUTS</span></span>

## <span data-ttu-id="ad59c-123">상속자</span><span class="sxs-lookup"><span data-stu-id="ad59c-123">NOTES</span></span>

## <span data-ttu-id="ad59c-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad59c-124">RELATED LINKS</span></span>

[<span data-ttu-id="ad59c-125">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="ad59c-125">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)


