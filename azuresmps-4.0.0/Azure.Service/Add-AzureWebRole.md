---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045711"
---
# <span data-ttu-id="5804c-101">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="5804c-101">Add-AzureWebRole</span></span>

## <span data-ttu-id="5804c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5804c-102">SYNOPSIS</span></span>
<span data-ttu-id="5804c-103">웹 작업자 역할을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-103">Adds a web worker role.</span></span>

## <span data-ttu-id="5804c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5804c-104">SYNTAX</span></span>

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5804c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5804c-105">DESCRIPTION</span></span>
<span data-ttu-id="5804c-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5804c-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5804c-108">**추가-AzureWebRole** cmdlet은 웹 작업자 역할을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-108">The **Add-AzureWebRole** cmdlet adds a web worker role.</span></span>

## <span data-ttu-id="5804c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5804c-109">EXAMPLES</span></span>

### <span data-ttu-id="5804c-110">예제 1: 기본 역할 추가</span><span class="sxs-lookup"><span data-stu-id="5804c-110">Example 1: Add a default role</span></span>
```
PS C:\> Add-AzureWebRole
```

<span data-ttu-id="5804c-111">이 명령은 Webrole1의 기본 구성이 있는 웹 역할을 이름 및 단일 인스턴스로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-111">This command add web role that has the default configuration of Webrole1 as the name and a single instance.</span></span>

### <span data-ttu-id="5804c-112">예제 2: 이름을 사용 하 여 역할 추가</span><span class="sxs-lookup"><span data-stu-id="5804c-112">Example 2: Add a role with a name</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

<span data-ttu-id="5804c-113">이 명령은 MyWebRole 이라는 단일 웹 역할을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-113">This command adds a single web role named MyWebRole to the current application.</span></span>

### <span data-ttu-id="5804c-114">예제 3: 이름 및 인스턴스 수를 사용 하 여 역할 추가</span><span class="sxs-lookup"><span data-stu-id="5804c-114">Example 3: Add a role with a name and instance count</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

<span data-ttu-id="5804c-115">이 명령은 MyWebRole 이라는 웹 역할을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-115">This command adds a web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="5804c-116">Cmdlet의 역할 인스턴스 수는 2입니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-116">The cmdlet has a role instance count of 2.</span></span>

### <span data-ttu-id="5804c-117">예제 4: 이름 및 서식 파일을 사용 하 여 역할 추가</span><span class="sxs-lookup"><span data-stu-id="5804c-117">Example 4: Add a role with a name and template</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

<span data-ttu-id="5804c-118">이 명령은 MyWebRole 이라는 단일 웹 역할을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-118">This command adds a single web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="5804c-119">명령에서 Myweb서식 파일 폴더를 스 캐 폴딩 템플릿으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-119">The command specifies a folder named MyWebTemplateFolder as a scaffolding template.</span></span>

## <span data-ttu-id="5804c-120">변수</span><span class="sxs-lookup"><span data-stu-id="5804c-120">PARAMETERS</span></span>

### <span data-ttu-id="5804c-121">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="5804c-121">-Instances</span></span>
<span data-ttu-id="5804c-122">인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-122">Specifies the number of instances.</span></span>

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

### <span data-ttu-id="5804c-123">-이름</span><span class="sxs-lookup"><span data-stu-id="5804c-123">-Name</span></span>
<span data-ttu-id="5804c-124">웹 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-124">Specifies the name of the web role.</span></span>

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

### <span data-ttu-id="5804c-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="5804c-125">-Profile</span></span>
<span data-ttu-id="5804c-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5804c-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5804c-128">-서식 폴더</span><span class="sxs-lookup"><span data-stu-id="5804c-128">-TemplateFolder</span></span>
<span data-ttu-id="5804c-129">서식 파일 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-129">Specifies the template folder.</span></span>

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

### <span data-ttu-id="5804c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5804c-130">CommonParameters</span></span>
<span data-ttu-id="5804c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5804c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5804c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5804c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5804c-133">입력</span><span class="sxs-lookup"><span data-stu-id="5804c-133">INPUTS</span></span>

## <span data-ttu-id="5804c-134">출력</span><span class="sxs-lookup"><span data-stu-id="5804c-134">OUTPUTS</span></span>

## <span data-ttu-id="5804c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5804c-135">NOTES</span></span>

## <span data-ttu-id="5804c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5804c-136">RELATED LINKS</span></span>

[<span data-ttu-id="5804c-137">추가-Azure역할</span><span class="sxs-lookup"><span data-stu-id="5804c-137">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)

[<span data-ttu-id="5804c-138">새로운 AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="5804c-138">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


