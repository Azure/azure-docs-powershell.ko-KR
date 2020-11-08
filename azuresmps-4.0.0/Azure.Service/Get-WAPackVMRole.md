---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047414"
---
# <span data-ttu-id="0d3ee-101">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0d3ee-101">Get-WAPackVMRole</span></span>

## <span data-ttu-id="0d3ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d3ee-102">SYNOPSIS</span></span>

## <span data-ttu-id="0d3ee-103">구문과</span><span class="sxs-lookup"><span data-stu-id="0d3ee-103">SYNTAX</span></span>

### <span data-ttu-id="0d3ee-104">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0d3ee-104">Empty (Default)</span></span>
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0d3ee-105">FromName</span><span class="sxs-lookup"><span data-stu-id="0d3ee-105">FromName</span></span>
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0d3ee-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="0d3ee-106">FromCloudService</span></span>
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d3ee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0d3ee-107">DESCRIPTION</span></span>
<span data-ttu-id="0d3ee-108">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="0d3ee-109">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0d3ee-110">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="0d3ee-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0d3ee-111">EXAMPLES</span></span>

### <span data-ttu-id="0d3ee-112">예제 1: 가상 컴퓨터 역할 가져오기 (포털을 통해 생성)</span><span class="sxs-lookup"><span data-stu-id="0d3ee-112">Example 1: Get a virtual machine role (created through the portal)</span></span>
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

<span data-ttu-id="0d3ee-113">이 명령은 ContosoVMRole01 이라는 포털을 통해 만들어진 가상 컴퓨터 역할을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-113">This command gets a virtual machine role which has been created through the portal named ContosoVMRole01.</span></span>

### <span data-ttu-id="0d3ee-114">예제 2: 이름 및 클라우드 서비스 이름을 사용 하 여 가상 컴퓨터 역할 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d3ee-114">Example 2: Get a virtual machine role by using a name and a cloud service name</span></span>
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

<span data-ttu-id="0d3ee-115">이 명령은 ContosoVMRole02 이라는 가상 컴퓨터 역할을 가져옵니다 .이는 ContosoCloudService01 라는 클라우드 서비스에서 스탠드 인.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-115">This command gets a virtual machine role named ContosoVMRole02 which stand on a cloud service named ContosoCloudService01.</span></span>

### <span data-ttu-id="0d3ee-116">예제 3: 모든 가상 컴퓨터 역할 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d3ee-116">Example 3: Get all virtual machine role</span></span>
```
PS C:\> Get-WAPackVMRole
```

<span data-ttu-id="0d3ee-117">이 명령은 모든 기존 가상 컴퓨터 역할을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-117">This command gets all existing virtual machine role.</span></span>

## <span data-ttu-id="0d3ee-118">변수</span><span class="sxs-lookup"><span data-stu-id="0d3ee-118">PARAMETERS</span></span>

### <span data-ttu-id="0d3ee-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="0d3ee-119">-CloudServiceName</span></span>
<span data-ttu-id="0d3ee-120">가상 컴퓨터 역할의 클라우드 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-120">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d3ee-121">-이름</span><span class="sxs-lookup"><span data-stu-id="0d3ee-121">-Name</span></span>
<span data-ttu-id="0d3ee-122">가상 컴퓨터 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-122">Specifies the name of a virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d3ee-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="0d3ee-123">-Profile</span></span>
<span data-ttu-id="0d3ee-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0d3ee-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0d3ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d3ee-126">CommonParameters</span></span>
<span data-ttu-id="0d3ee-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d3ee-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d3ee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d3ee-129">입력</span><span class="sxs-lookup"><span data-stu-id="0d3ee-129">INPUTS</span></span>

## <span data-ttu-id="0d3ee-130">출력</span><span class="sxs-lookup"><span data-stu-id="0d3ee-130">OUTPUTS</span></span>

## <span data-ttu-id="0d3ee-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0d3ee-131">NOTES</span></span>

## <span data-ttu-id="0d3ee-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d3ee-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d3ee-133">새로운 WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0d3ee-133">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="0d3ee-134">제거-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0d3ee-134">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="0d3ee-135">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0d3ee-135">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


