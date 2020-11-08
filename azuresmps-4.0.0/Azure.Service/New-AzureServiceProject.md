---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046218"
---
# <span data-ttu-id="2effa-101">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="2effa-101">New-AzureServiceProject</span></span>

## <span data-ttu-id="2effa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2effa-102">SYNOPSIS</span></span>
<span data-ttu-id="2effa-103">새 서비스에 필요한 파일과 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-103">Creates the required files and configuration for a new service.</span></span>

## <span data-ttu-id="2effa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2effa-104">SYNTAX</span></span>

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2effa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2effa-105">DESCRIPTION</span></span>
<span data-ttu-id="2effa-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2effa-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2effa-108">**새로운-AzureServiceProject** cmdlet은 현재 디렉터리에 새 Azure 서비스에 대 한 필수 파일과 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-108">The **New-AzureServiceProject** cmdlet creates the required files and configuration for a new Azure service in the current directory.</span></span>

## <span data-ttu-id="2effa-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2effa-109">EXAMPLES</span></span>

### <span data-ttu-id="2effa-110">예제 1: 서비스에 대 한 스 캐 폴딩 만들기</span><span class="sxs-lookup"><span data-stu-id="2effa-110">Example 1: Create scaffolding for a service</span></span>
```
PS C:\> New-AzureServiceProject MyService1
```

<span data-ttu-id="2effa-111">이 예제에서는 현재 디렉터리에 MyService1 이라는 새 Azure 서비스에 대 한 스 캐 폴딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-111">This example creates scaffolding for a new Azure service named MyService1 in the current directory.</span></span>

## <span data-ttu-id="2effa-112">변수</span><span class="sxs-lookup"><span data-stu-id="2effa-112">PARAMETERS</span></span>

### <span data-ttu-id="2effa-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="2effa-113">-Profile</span></span>
<span data-ttu-id="2effa-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2effa-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2effa-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2effa-116">-ServiceName</span></span>
<span data-ttu-id="2effa-117">서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-117">Specifies the name of the service.</span></span>
<span data-ttu-id="2effa-118">서비스의 호스트 이름 (예: name.cloudapp.net)과 서비스를 포함 하는 디렉터리의 첫 번째 섹션을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-118">It determines the first section of the hostname for your service (for example, name.cloudapp.net), and the directory that will contain your service.</span></span>
<span data-ttu-id="2effa-119">이름에는 문자, 숫자 및 대시 문자 (-)만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-119">The name can contain only letters, digits, and the dash character (-).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2effa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2effa-120">CommonParameters</span></span>
<span data-ttu-id="2effa-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2effa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2effa-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2effa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2effa-123">입력</span><span class="sxs-lookup"><span data-stu-id="2effa-123">INPUTS</span></span>

## <span data-ttu-id="2effa-124">출력</span><span class="sxs-lookup"><span data-stu-id="2effa-124">OUTPUTS</span></span>

## <span data-ttu-id="2effa-125">상속자</span><span class="sxs-lookup"><span data-stu-id="2effa-125">NOTES</span></span>

## <span data-ttu-id="2effa-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2effa-126">RELATED LINKS</span></span>

[<span data-ttu-id="2effa-127">추가-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="2effa-127">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="2effa-128">추가-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="2effa-128">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="2effa-129">게시-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="2effa-129">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="2effa-130">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="2effa-130">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)

[<span data-ttu-id="2effa-131">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="2effa-131">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


