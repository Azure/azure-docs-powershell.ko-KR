---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046387"
---
# <span data-ttu-id="c5311-101">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="c5311-101">Add-AzurePHPWorkerRole</span></span>

## <span data-ttu-id="c5311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5311-102">SYNOPSIS</span></span>
<span data-ttu-id="c5311-103">Azure에서 php.exe에 호스팅되는 PHP 응용 프로그램에 필요한 파일과 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-103">Creates the required files and configuration for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="c5311-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5311-104">SYNTAX</span></span>

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c5311-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c5311-105">DESCRIPTION</span></span>
<span data-ttu-id="c5311-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c5311-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c5311-108">Azure에서 php.exe에 호스팅되는 PHP 응용 프로그램에 필요한 파일 및 구성 (스 캐 폴딩이 라고도 함)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-108">Creates the required files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="c5311-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c5311-109">EXAMPLES</span></span>

### <span data-ttu-id="c5311-110">예제 1: 단일 인스턴스를 사용 하 여 작업자 역할 만들기</span><span class="sxs-lookup"><span data-stu-id="c5311-110">Example 1: Create a worker role with a single instance</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

<span data-ttu-id="c5311-111">이 예제에서는 My이라는 역할을 하는 단일 작업자 역할에 대 한 필수 파일과 구성을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-111">This example adds the required files and configuration for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="c5311-112">예제 2: 여러 인스턴스를 사용 하 여 작업자 역할 만들기</span><span class="sxs-lookup"><span data-stu-id="c5311-112">Example 2: Create a worker role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="c5311-113">이 예제에서는 역할 인스턴스 수가 2 인 My: name 역할을 사용 하 여 새 작업자 역할에 대 한 필수 파일과 구성을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-113">This example adds the required files and configuration for a new worker role to the current application, using the name MyWorkerRole with a role instance count of 2.</span></span>

## <span data-ttu-id="c5311-114">변수</span><span class="sxs-lookup"><span data-stu-id="c5311-114">PARAMETERS</span></span>

### <span data-ttu-id="c5311-115">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="c5311-115">-Instances</span></span>
<span data-ttu-id="c5311-116">이 작업자 역할에 대 한 역할 인스턴스의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="c5311-117">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-117">The default is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5311-118">-이름</span><span class="sxs-lookup"><span data-stu-id="c5311-118">-Name</span></span>
<span data-ttu-id="c5311-119">작업자 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="c5311-120">이름에는 작업자 역할에 호스팅되는 PHP 서비스에 대 한 필수 파일 및 구성이 포함 된 폴더 이름이 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-120">The name determines the folder name that contains the required files and configuration for the PHP service hosted in the worker role.</span></span>
<span data-ttu-id="c5311-121">기본값은 WorkerRole1입니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-121">The default is WorkerRole1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5311-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="c5311-122">-Profile</span></span>
<span data-ttu-id="c5311-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5311-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5311-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5311-125">CommonParameters</span></span>
<span data-ttu-id="c5311-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5311-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5311-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5311-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5311-128">입력</span><span class="sxs-lookup"><span data-stu-id="c5311-128">INPUTS</span></span>

## <span data-ttu-id="c5311-129">출력</span><span class="sxs-lookup"><span data-stu-id="c5311-129">OUTPUTS</span></span>

## <span data-ttu-id="c5311-130">상속자</span><span class="sxs-lookup"><span data-stu-id="c5311-130">NOTES</span></span>

## <span data-ttu-id="c5311-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5311-131">RELATED LINKS</span></span>

[<span data-ttu-id="c5311-132">새-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="c5311-132">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="c5311-133">추가-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="c5311-133">Add-AzurePHPWebRole</span></span>](./Add-AzurePHPWebRole.md)


