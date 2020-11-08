---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03acdfb16c7f1e7e8ee5e6b95902ef1ed056412a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045458"
---
# <span data-ttu-id="c17eb-101">Save-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="c17eb-101">Save-AzureWebsiteLog</span></span>

## <span data-ttu-id="c17eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c17eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c17eb-103">지정 된 웹 사이트의 로그를 다운로드 하 여 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-103">Downloads and saves the logs for a specified website.</span></span>

## <span data-ttu-id="c17eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c17eb-104">SYNTAX</span></span>

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c17eb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c17eb-105">DESCRIPTION</span></span>
<span data-ttu-id="c17eb-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c17eb-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c17eb-108">**AzureWebsiteLog** cmdlet은 지정 된 웹 사이트의 로그를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-108">The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.</span></span>

## <span data-ttu-id="c17eb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c17eb-109">EXAMPLES</span></span>

### <span data-ttu-id="c17eb-110">예제 1: 웹 사이트의 로그 다운로드 및 저장</span><span class="sxs-lookup"><span data-stu-id="c17eb-110">Example 1: Download and save logs for a website</span></span>
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

<span data-ttu-id="c17eb-111">이 예제에서는 웹 사이트 내에 대 한 런타임 및 배포 로그를 현재 디렉터리의 파일 logs.zip으로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-111">This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.</span></span>

## <span data-ttu-id="c17eb-112">변수</span><span class="sxs-lookup"><span data-stu-id="c17eb-112">PARAMETERS</span></span>

### <span data-ttu-id="c17eb-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c17eb-113">-Name</span></span>
<span data-ttu-id="c17eb-114">웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-114">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="c17eb-115">-출력</span><span class="sxs-lookup"><span data-stu-id="c17eb-115">-Output</span></span>
<span data-ttu-id="c17eb-116">다운로드 한 파일을 저장할 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-116">Specifies the path to store the downloaded file.</span></span>

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

### <span data-ttu-id="c17eb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c17eb-117">-PassThru</span></span>
<span data-ttu-id="c17eb-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c17eb-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c17eb-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="c17eb-120">-Profile</span></span>
<span data-ttu-id="c17eb-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c17eb-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c17eb-123">-슬롯</span><span class="sxs-lookup"><span data-stu-id="c17eb-123">-Slot</span></span>
<span data-ttu-id="c17eb-124">슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="c17eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17eb-125">CommonParameters</span></span>
<span data-ttu-id="c17eb-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17eb-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c17eb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17eb-128">입력</span><span class="sxs-lookup"><span data-stu-id="c17eb-128">INPUTS</span></span>

## <span data-ttu-id="c17eb-129">출력</span><span class="sxs-lookup"><span data-stu-id="c17eb-129">OUTPUTS</span></span>

## <span data-ttu-id="c17eb-130">상속자</span><span class="sxs-lookup"><span data-stu-id="c17eb-130">NOTES</span></span>

## <span data-ttu-id="c17eb-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c17eb-131">RELATED LINKS</span></span>

[<span data-ttu-id="c17eb-132">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="c17eb-132">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


