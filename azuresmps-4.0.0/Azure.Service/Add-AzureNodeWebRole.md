---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046392"
---
# <span data-ttu-id="b82db-101">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="b82db-101">Add-AzureNodeWebRole</span></span>

## <span data-ttu-id="b82db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b82db-102">SYNOPSIS</span></span>
<span data-ttu-id="b82db-103">Node.js 응용 프로그램에 필요한 파일과 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-103">Creates required files and folders for a Node.js application.</span></span>

## <span data-ttu-id="b82db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b82db-104">SYNTAX</span></span>

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b82db-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b82db-105">DESCRIPTION</span></span>
<span data-ttu-id="b82db-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b82db-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b82db-108">AzureNodeWebRole는 IIS를 통해 클라우드에서 호스팅될 Node.js 응용 프로그램에 대해 필요한 파일과 폴더 (스 캐 폴딩이 라고도 함 **)** 를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-108">The **Add-AzureNodeWebRole** creates required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via IIS.</span></span>

## <span data-ttu-id="b82db-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b82db-109">EXAMPLES</span></span>

### <span data-ttu-id="b82db-110">예제 1: 단일 인스턴스 웹 역할</span><span class="sxs-lookup"><span data-stu-id="b82db-110">Example 1: Single instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

<span data-ttu-id="b82db-111">이 예제에서는 **MyWebRole** 라는 단일 웹 역할에 대 한 스 캐 폴딩을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-111">This example adds scaffolding for a single web role named **MyWebRole** to the current application.</span></span>

### <span data-ttu-id="b82db-112">예제 2: 여러 인스턴스 웹 역할</span><span class="sxs-lookup"><span data-stu-id="b82db-112">Example 2: Multiple instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

<span data-ttu-id="b82db-113">이 예제에서는 역할 인스턴스 수가 2 인 **MyWebRole** 이라는 새 웹 역할에 대 한 스 캐 폴딩을 현재 응용 프로그램에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-113">This example adds scaffolding for a new web role named **MyWebRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="b82db-114">변수</span><span class="sxs-lookup"><span data-stu-id="b82db-114">PARAMETERS</span></span>

### <span data-ttu-id="b82db-115">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="b82db-115">-Instances</span></span>
<span data-ttu-id="b82db-116">이 웹 역할에 대 한 역할 인스턴스의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="b82db-117">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-117">The default is 1.</span></span>

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

### <span data-ttu-id="b82db-118">-이름</span><span class="sxs-lookup"><span data-stu-id="b82db-118">-Name</span></span>
<span data-ttu-id="b82db-119">웹 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="b82db-120">또한 웹 역할에서 호스팅될 node.js 응용 프로그램에 대 한 스 캐 폴딩이 포함 된 디렉터리의 이름을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-120">It also determines the name of the directory that contains the scaffolding for the node.js application that will be hosted in the web role.</span></span>
<span data-ttu-id="b82db-121">기본값은 WebRole # 이며, 여기서 #은 서비스의 웹 역할 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-121">The default is WebRole#, where # indicates the number of web roles in the service.</span></span>

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

### <span data-ttu-id="b82db-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="b82db-122">-Profile</span></span>
<span data-ttu-id="b82db-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b82db-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b82db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82db-125">CommonParameters</span></span>
<span data-ttu-id="b82db-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82db-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b82db-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82db-128">입력</span><span class="sxs-lookup"><span data-stu-id="b82db-128">INPUTS</span></span>

## <span data-ttu-id="b82db-129">출력</span><span class="sxs-lookup"><span data-stu-id="b82db-129">OUTPUTS</span></span>

## <span data-ttu-id="b82db-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b82db-130">NOTES</span></span>

## <span data-ttu-id="b82db-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b82db-131">RELATED LINKS</span></span>

[<span data-ttu-id="b82db-132">추가-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="b82db-132">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="b82db-133">새-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="b82db-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


