---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045710"
---
# <span data-ttu-id="dc162-101">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="dc162-101">Add-AzureWorkerRole</span></span>

## <span data-ttu-id="dc162-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc162-102">SYNOPSIS</span></span>
<span data-ttu-id="dc162-103">사용자 지정 작업자 역할에 필요한 파일과 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-103">Creates required files and configuration for a custom worker role.</span></span>

## <span data-ttu-id="dc162-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc162-104">SYNTAX</span></span>

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc162-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dc162-105">DESCRIPTION</span></span>
<span data-ttu-id="dc162-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="dc162-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="dc162-108">**추가-azure역할** cmdlet은 사용자 지정 작업자 역할에 대해 필요한 파일과 구성을 만듭니다 (스 캐 폴딩이 라고도 함).</span><span class="sxs-lookup"><span data-stu-id="dc162-108">The **Add-AzureWorkerRole** cmdlet creates required files and configuration, sometimes referred to as scaffolding, for a custom worker role.</span></span>

## <span data-ttu-id="dc162-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dc162-109">EXAMPLES</span></span>

### <span data-ttu-id="dc162-110">예제 1: 단일 인스턴스 작업자 역할 만들기</span><span class="sxs-lookup"><span data-stu-id="dc162-110">Example 1: Create a single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

<span data-ttu-id="dc162-111">이 예제에서는 My현 역할 이라는 단일 작업자 역할에 대 한 스 캐 폴딩을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-111">This example adds scaffolding for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="dc162-112">예제 2: 다중 인스턴스 작업자 역할 만들기</span><span class="sxs-lookup"><span data-stu-id="dc162-112">Example 2: Create a multiple instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="dc162-113">이 예제에서는 역할 인스턴스 수가 2 인 Myount 역할 이라는 새 작업자 역할에 대 한 스 캐 폴딩을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-113">This example adds scaffolding for a new worker role named MyWorkerRole to the current application, with a role instance count of 2.</span></span>

### <span data-ttu-id="dc162-114">예제 3: 사용자 지정 스 캐 폴딩을 사용 하 여 작업자 역할 만들기</span><span class="sxs-lookup"><span data-stu-id="dc162-114">Example 3: Create worker role with custom scaffolding</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

<span data-ttu-id="dc162-115">이 예제에서는 사용자 지정 스 캐 폴딩이 있는 작업자 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-115">This example creates a worker role with custom scaffolding.</span></span>

## <span data-ttu-id="dc162-116">변수</span><span class="sxs-lookup"><span data-stu-id="dc162-116">PARAMETERS</span></span>

### <span data-ttu-id="dc162-117">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="dc162-117">-Instances</span></span>
<span data-ttu-id="dc162-118">이 작업자 역할에 대 한 역할 인스턴스의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-118">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="dc162-119">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-119">The default is 1.</span></span>

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

### <span data-ttu-id="dc162-120">-이름</span><span class="sxs-lookup"><span data-stu-id="dc162-120">-Name</span></span>
<span data-ttu-id="dc162-121">작업자 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-121">Specifies the name of the worker role.</span></span>
<span data-ttu-id="dc162-122">이 값은 작업자 역할에 호스팅되는 사용자 지정 응용 프로그램의 스 캐 폴딩을 포함 하는 폴더 이름을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-122">This value determines the folder name that contains the scaffolding for the custom application that will be hosted in the worker role.</span></span>
<span data-ttu-id="dc162-123">기본값은 WorkerRolenumber 이며, 여기에서 number는 서비스의 작업자 역할 수입니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-123">The default is WorkerRolenumber, where number is the number of worker roles in the service.</span></span>

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

### <span data-ttu-id="dc162-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="dc162-124">-Profile</span></span>
<span data-ttu-id="dc162-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc162-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc162-127">-서식 폴더</span><span class="sxs-lookup"><span data-stu-id="dc162-127">-TemplateFolder</span></span>
<span data-ttu-id="dc162-128">작업자 역할을 만드는 데 사용할 스 캐 폴딩 템플릿 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-128">Specifies the scaffolding template folder to be used to create the worker role.</span></span>

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

### <span data-ttu-id="dc162-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc162-129">CommonParameters</span></span>
<span data-ttu-id="dc162-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc162-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc162-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc162-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc162-132">입력</span><span class="sxs-lookup"><span data-stu-id="dc162-132">INPUTS</span></span>

## <span data-ttu-id="dc162-133">출력</span><span class="sxs-lookup"><span data-stu-id="dc162-133">OUTPUTS</span></span>

## <span data-ttu-id="dc162-134">상속자</span><span class="sxs-lookup"><span data-stu-id="dc162-134">NOTES</span></span>

## <span data-ttu-id="dc162-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc162-135">RELATED LINKS</span></span>

[<span data-ttu-id="dc162-136">추가-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="dc162-136">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="dc162-137">새로운 AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="dc162-137">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


