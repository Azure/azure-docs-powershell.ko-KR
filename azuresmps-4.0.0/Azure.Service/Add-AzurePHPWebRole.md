---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046390"
---
# <span data-ttu-id="01da5-101">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="01da5-101">Add-AzurePHPWebRole</span></span>

## <span data-ttu-id="01da5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01da5-102">SYNOPSIS</span></span>
<span data-ttu-id="01da5-103">PHP 응용 프로그램에 필요한 파일과 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-103">Creates the required files and configuration for a PHP application.</span></span>

## <span data-ttu-id="01da5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01da5-104">SYNTAX</span></span>

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="01da5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01da5-105">DESCRIPTION</span></span>
<span data-ttu-id="01da5-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="01da5-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="01da5-108">AzurePHPWebRole cmdlet은 Azure에서 IIS를 통해 호스팅되는 PHP 응용 프로그램에 대 한 파일 및 구성 (스 캐 폴딩이 라고도 함 **)** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-108">The **Add-AzurePHPWebRole** cmdlet creates the files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through IIS.</span></span>

## <span data-ttu-id="01da5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="01da5-109">EXAMPLES</span></span>

### <span data-ttu-id="01da5-110">예제 1: 기본 값을 사용 하 여 웹 역할 추가</span><span class="sxs-lookup"><span data-stu-id="01da5-110">Example 1: Add a web role using default values</span></span>
```
PS C:\> Add-AzurePHPWebRole
```

<span data-ttu-id="01da5-111">이 예제에서는 "WebRole1" 이라는 서비스의 기본값을 1 개 인스턴스와 함께 사용 하 여 새 웹 역할에 필요한 파일과 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-111">This example adds the required files and configuration for new web role using the default values of a service named "WebRole1" with 1 instance.</span></span>

### <span data-ttu-id="01da5-112">예제 2: 여러 인스턴스가 있는 웹 역할 추가</span><span class="sxs-lookup"><span data-stu-id="01da5-112">Example 2: Add a web role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

<span data-ttu-id="01da5-113">이 예제에서는 새 웹 역할에 대 한 필수 파일 및 구성을 "MyWebRole" 이름 및 역할 인스턴스 수 2를 사용 하 여 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-113">This example adds the required files and configuration for a new web role to the current application, using the name "MyWebRole" and a role instance count of 2.</span></span>

## <span data-ttu-id="01da5-114">변수</span><span class="sxs-lookup"><span data-stu-id="01da5-114">PARAMETERS</span></span>

### <span data-ttu-id="01da5-115">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="01da5-115">-Instances</span></span>
<span data-ttu-id="01da5-116">이 웹 역할에 대 한 역할 인스턴스의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="01da5-117">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-117">The default is 1.</span></span>

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

### <span data-ttu-id="01da5-118">-이름</span><span class="sxs-lookup"><span data-stu-id="01da5-118">-Name</span></span>
<span data-ttu-id="01da5-119">웹 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="01da5-120">이름에는 PHP 응용 프로그램에 대 한 필수 파일 및 구성이 포함 된 디렉터리의 이름이 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-120">The name determines the name of the directory that contains the required files and configuration for the PHP application.</span></span>
<span data-ttu-id="01da5-121">기본값은 WebRole # 이며 여기서 #은 서비스의 웹 역할 수입니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-121">The default is WebRole#, where # is the number of web roles in the service.</span></span>

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

### <span data-ttu-id="01da5-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="01da5-122">-Profile</span></span>
<span data-ttu-id="01da5-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="01da5-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01da5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01da5-125">CommonParameters</span></span>
<span data-ttu-id="01da5-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01da5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01da5-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01da5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01da5-128">입력</span><span class="sxs-lookup"><span data-stu-id="01da5-128">INPUTS</span></span>

## <span data-ttu-id="01da5-129">출력</span><span class="sxs-lookup"><span data-stu-id="01da5-129">OUTPUTS</span></span>

## <span data-ttu-id="01da5-130">상속자</span><span class="sxs-lookup"><span data-stu-id="01da5-130">NOTES</span></span>

## <span data-ttu-id="01da5-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01da5-131">RELATED LINKS</span></span>

[<span data-ttu-id="01da5-132">추가-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="01da5-132">Add-AzurePHPWorkerRole</span></span>](./Add-AzurePHPWorkerRole.md)

[<span data-ttu-id="01da5-133">새-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="01da5-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


