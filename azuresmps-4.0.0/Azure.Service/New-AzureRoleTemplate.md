---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045992"
---
# <span data-ttu-id="83fd1-101">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="83fd1-101">New-AzureRoleTemplate</span></span>

## <span data-ttu-id="83fd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="83fd1-103">웹 및 작업자 역할 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-103">Creates web and worker role templates.</span></span>

## <span data-ttu-id="83fd1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83fd1-104">SYNTAX</span></span>

### <span data-ttu-id="83fd1-105">WebRole</span><span class="sxs-lookup"><span data-stu-id="83fd1-105">WebRole</span></span>
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="83fd1-106">역할</span><span class="sxs-lookup"><span data-stu-id="83fd1-106">WorkerRole</span></span>
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="83fd1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="83fd1-107">DESCRIPTION</span></span>
<span data-ttu-id="83fd1-108">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="83fd1-109">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="83fd1-110">**새 AzureRoleTemplate** cmdlet은 웹 및 작업자 역할 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-110">The **New-AzureRoleTemplate** cmdlet creates web and worker role templates.</span></span>

## <span data-ttu-id="83fd1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="83fd1-111">EXAMPLES</span></span>

### <span data-ttu-id="83fd1-112">예제 1: 웹 역할 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="83fd1-112">Example 1: Create a web role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Web
```

<span data-ttu-id="83fd1-113">이 예제에서는 현재 디렉터리에 WebRoleTemplate 이라는 폴더에 새 웹 역할 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-113">This example creates a new web role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="83fd1-114">예제 2: 작업자 역할 템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="83fd1-114">Example 2: Create a worker role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Worker
```

<span data-ttu-id="83fd1-115">이 예제에서는 현재 디렉터리의 WebRoleTemplate 이라는 폴더에 새 작업자 역할 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-115">This example creates a new worker role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="83fd1-116">예제 3: 사용자 지정 디렉터리에 역할 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="83fd1-116">Example 3: Create a role template in a custom directory</span></span>
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

<span data-ttu-id="83fd1-117">이 예제에서는 현재 디렉토리가 아닌 MyWebRoleTemplate 이라는 디렉터리에 새 웹 역할 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-117">This example creates a new web role template in directory named MyWebRoleTemplate, instead of in the current directory.</span></span>

## <span data-ttu-id="83fd1-118">변수</span><span class="sxs-lookup"><span data-stu-id="83fd1-118">PARAMETERS</span></span>

### <span data-ttu-id="83fd1-119">-출력</span><span class="sxs-lookup"><span data-stu-id="83fd1-119">-Output</span></span>
<span data-ttu-id="83fd1-120">생성 된 템플릿의 출력 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-120">Specifies the output path of generated template.</span></span>

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

### <span data-ttu-id="83fd1-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="83fd1-121">-Profile</span></span>
<span data-ttu-id="83fd1-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83fd1-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83fd1-124">-웹</span><span class="sxs-lookup"><span data-stu-id="83fd1-124">-Web</span></span>
<span data-ttu-id="83fd1-125">웹 역할 서식 파일을 만들도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-125">Specifies that you want to create a web role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83fd1-126">-Worker</span><span class="sxs-lookup"><span data-stu-id="83fd1-126">-Worker</span></span>
<span data-ttu-id="83fd1-127">작업자 역할 템플릿을 만들지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-127">Specifies that you want to create a worker role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83fd1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fd1-128">CommonParameters</span></span>
<span data-ttu-id="83fd1-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fd1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fd1-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83fd1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fd1-131">입력</span><span class="sxs-lookup"><span data-stu-id="83fd1-131">INPUTS</span></span>

## <span data-ttu-id="83fd1-132">출력</span><span class="sxs-lookup"><span data-stu-id="83fd1-132">OUTPUTS</span></span>

## <span data-ttu-id="83fd1-133">상속자</span><span class="sxs-lookup"><span data-stu-id="83fd1-133">NOTES</span></span>

## <span data-ttu-id="83fd1-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83fd1-134">RELATED LINKS</span></span>

[<span data-ttu-id="83fd1-135">추가-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="83fd1-135">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="83fd1-136">추가-Azure역할</span><span class="sxs-lookup"><span data-stu-id="83fd1-136">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)


