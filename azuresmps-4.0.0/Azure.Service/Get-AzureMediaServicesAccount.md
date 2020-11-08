---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046335"
---
# <span data-ttu-id="1d48c-101">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1d48c-101">Get-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="1d48c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d48c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d48c-103">사용할 수 있는 Azure Media 서비스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-103">Gets the available Azure Media Services accounts.</span></span>

<span data-ttu-id="1d48c-104">**참고:** 이 버전은 더 이상 사용 되지 않습니다. [최신 버전](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="1d48c-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="1d48c-105">구문과</span><span class="sxs-lookup"><span data-stu-id="1d48c-105">SYNTAX</span></span>

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1d48c-106">설명은</span><span class="sxs-lookup"><span data-stu-id="1d48c-106">DESCRIPTION</span></span>
<span data-ttu-id="1d48c-107">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1d48c-108">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1d48c-109">모든 계정을 나열 하려면 cmdlet을 사용 `Get-AzureMediaServicesAccount` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-109">To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.</span></span>
<span data-ttu-id="1d48c-110">특정 계정에 대 한 자세한 정보를 보려면 cmdlet을 사용 `Get-AzureMediaServicesAccount -Name YourAccountName` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-110">To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span></span>

## <span data-ttu-id="1d48c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1d48c-111">EXAMPLES</span></span>

### <span data-ttu-id="1d48c-112">예제 1: 모든 미디어 서비스 계정 나열</span><span class="sxs-lookup"><span data-stu-id="1d48c-112">Example 1: List all Media Services accounts</span></span>
```
PS C:\> Get-AzureMediaServicesAccount
```

<span data-ttu-id="1d48c-113">이 명령은 사용 가능한 모든 미디어 서비스 계정을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-113">This command lists all available Media Services accounts.</span></span>

### <span data-ttu-id="1d48c-114">예제 2: 미디어 서비스 계정에 대 한 자세한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="1d48c-114">Example 2: Get detailed information about a Media Services account</span></span>
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

<span data-ttu-id="1d48c-115">이 명령은 미디어 서비스 계정의 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-115">This command displays properties of a Media Services account.</span></span>

## <span data-ttu-id="1d48c-116">변수</span><span class="sxs-lookup"><span data-stu-id="1d48c-116">PARAMETERS</span></span>

### <span data-ttu-id="1d48c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="1d48c-117">-Name</span></span>
<span data-ttu-id="1d48c-118">미디어 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-118">The Media Services account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d48c-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="1d48c-119">-Profile</span></span>
<span data-ttu-id="1d48c-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1d48c-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1d48c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d48c-122">CommonParameters</span></span>
<span data-ttu-id="1d48c-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d48c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d48c-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d48c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d48c-125">입력</span><span class="sxs-lookup"><span data-stu-id="1d48c-125">INPUTS</span></span>

## <span data-ttu-id="1d48c-126">출력</span><span class="sxs-lookup"><span data-stu-id="1d48c-126">OUTPUTS</span></span>

## <span data-ttu-id="1d48c-127">상속자</span><span class="sxs-lookup"><span data-stu-id="1d48c-127">NOTES</span></span>

## <span data-ttu-id="1d48c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d48c-128">RELATED LINKS</span></span>

[<span data-ttu-id="1d48c-129">미디어 서비스에 Azure PowerShell을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1d48c-129">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


