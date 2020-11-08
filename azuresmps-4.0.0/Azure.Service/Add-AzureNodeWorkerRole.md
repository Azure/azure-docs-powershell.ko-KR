---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046389"
---
# <span data-ttu-id="999cf-101">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="999cf-101">Add-AzureNodeWorkerRole</span></span>

## <span data-ttu-id="999cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="999cf-102">SYNOPSIS</span></span>
<span data-ttu-id="999cf-103">node.exe를 통해 클라우드에서 호스팅될 Node.js 응용 프로그램에 필요한 파일과 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-103">Creates the required files and folders for a Node.js application to be hosted in the cloud via node.exe</span></span>

## <span data-ttu-id="999cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="999cf-104">SYNTAX</span></span>

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="999cf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="999cf-105">DESCRIPTION</span></span>
<span data-ttu-id="999cf-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="999cf-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="999cf-108">AzureNodeWorkerRole cmdlet은 node.exe를 통해 클라우드에서 호스팅되는 Node.js 응용 프로그램에 대해 필요한 파일과 폴더 (스 캐 폴딩이 라고도 함 **)** 를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-108">The **Add-AzureNodeWorkerRole** cmdlet creates the required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via node.exe.</span></span>

## <span data-ttu-id="999cf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="999cf-109">EXAMPLES</span></span>

### <span data-ttu-id="999cf-110">예제 1: 단일 인스턴스 작업자 역할</span><span class="sxs-lookup"><span data-stu-id="999cf-110">Example 1: Single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

<span data-ttu-id="999cf-111">이 예제에서는 **my현 역할** 이라는 단일 작업자 역할에 대 한 스 캐 폴딩을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-111">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application.</span></span>

### <span data-ttu-id="999cf-112">예제 2: 여러 인스턴스 작업자 역할</span><span class="sxs-lookup"><span data-stu-id="999cf-112">Example 2: Multiple instance worker role</span></span>
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="999cf-113">이 예제에서는 역할 인스턴스 수가 2 인 **Myount 역할** 이라는 단일 작업자 역할에 대 한 스 캐 폴딩을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-113">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="999cf-114">변수</span><span class="sxs-lookup"><span data-stu-id="999cf-114">PARAMETERS</span></span>

### <span data-ttu-id="999cf-115">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="999cf-115">-Instances</span></span>
<span data-ttu-id="999cf-116">이 작업자 역할에 대 한 역할 인스턴스의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="999cf-117">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-117">Default is 1.</span></span>

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

### <span data-ttu-id="999cf-118">-이름</span><span class="sxs-lookup"><span data-stu-id="999cf-118">-Name</span></span>
<span data-ttu-id="999cf-119">작업자 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="999cf-120">값은 작업자 역할에 호스팅되는 node.js 서비스에 대 한 스 캐 폴딩을 포함 하는 폴더 이름을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-120">The value determines the folder name that contains the scaffolding for the node.js service hosted in the worker role.</span></span>
<span data-ttu-id="999cf-121">기본값은 WorkerRole1입니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-121">Default is WorkerRole1.</span></span>

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

### <span data-ttu-id="999cf-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="999cf-122">-Profile</span></span>
<span data-ttu-id="999cf-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="999cf-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="999cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="999cf-125">CommonParameters</span></span>
<span data-ttu-id="999cf-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="999cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="999cf-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="999cf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="999cf-128">입력</span><span class="sxs-lookup"><span data-stu-id="999cf-128">INPUTS</span></span>

## <span data-ttu-id="999cf-129">출력</span><span class="sxs-lookup"><span data-stu-id="999cf-129">OUTPUTS</span></span>

## <span data-ttu-id="999cf-130">상속자</span><span class="sxs-lookup"><span data-stu-id="999cf-130">NOTES</span></span>

## <span data-ttu-id="999cf-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="999cf-131">RELATED LINKS</span></span>

[<span data-ttu-id="999cf-132">추가-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="999cf-132">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="999cf-133">새-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="999cf-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


