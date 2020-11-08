---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047390"
---
# <span data-ttu-id="9166c-101">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="9166c-101">New-WAPackVMRole</span></span>

## <span data-ttu-id="9166c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9166c-102">SYNOPSIS</span></span>
<span data-ttu-id="9166c-103">가상 컴퓨터 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-103">Creates a virtual machine role.</span></span>

## <span data-ttu-id="9166c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9166c-104">SYNTAX</span></span>

### <span data-ttu-id="9166c-105">빠른 만들기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9166c-105">QuickCreate (Default)</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9166c-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="9166c-106">FromCloudService</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9166c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9166c-107">DESCRIPTION</span></span>
<span data-ttu-id="9166c-108">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9166c-109">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9166c-110">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9166c-111">**새 WAPackVMRole** cmdlet은 가상 컴퓨터 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-111">The **New-WAPackVMRole** cmdlet creates a virtual machine role.</span></span>

## <span data-ttu-id="9166c-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9166c-112">EXAMPLES</span></span>

### <span data-ttu-id="9166c-113">예제 1: 가상 컴퓨터 역할 만들기 (WAP 동작 에뮬레이트)</span><span class="sxs-lookup"><span data-stu-id="9166c-113">Example 1: Create a virtual machine role (emulating WAP behavior)</span></span>
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

<span data-ttu-id="9166c-114">모든 클라우드 서비스를 지정 하지 않았으므로 (WAP 동작 에뮬레이트)이 명령은 가상 컴퓨터 역할과 동일한 이름을 가질 수 있도록 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-114">Since we do not specify any cloud service (emulating WAP behavior), the command will create a cloud service for us which will have the same name as the virtual machine role.</span></span>
<span data-ttu-id="9166c-115">이 경우 다음 명령을 사용 하면 이름 ContosoVMRole01, 레이블 ContosoVMRoleLabel01으로 가상 컴퓨터 역할이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-115">In this case, the following command will create a virtual machine role with the name ContosoVMRole01, label ContosoVMRoleLabel01.</span></span>
<span data-ttu-id="9166c-116">여기에서 사용 되는 리소스 정의는 PowerShell을 통해 수동으로 만들어야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="9166c-116">Note that the resource definition being used here has to be manually created though PowerShell.</span></span>

## <span data-ttu-id="9166c-117">변수</span><span class="sxs-lookup"><span data-stu-id="9166c-117">PARAMETERS</span></span>

### <span data-ttu-id="9166c-118">-CloudService</span><span class="sxs-lookup"><span data-stu-id="9166c-118">-CloudService</span></span>
<span data-ttu-id="9166c-119">가상 컴퓨터 역할에 대 한 클라우드 서비스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-119">Specifies a cloud service for the virtual machine role.</span></span>

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9166c-120">-레이블</span><span class="sxs-lookup"><span data-stu-id="9166c-120">-Label</span></span>
<span data-ttu-id="9166c-121">가상 컴퓨터 역할의 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-121">Specifies a label for the virtual machine role.</span></span>

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

### <span data-ttu-id="9166c-122">-이름</span><span class="sxs-lookup"><span data-stu-id="9166c-122">-Name</span></span>
<span data-ttu-id="9166c-123">가상 컴퓨터 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-123">Specifies a name for the virtual machine role.</span></span>

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

### <span data-ttu-id="9166c-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="9166c-124">-Profile</span></span>
<span data-ttu-id="9166c-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9166c-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9166c-127">-ResourceDefinition</span><span class="sxs-lookup"><span data-stu-id="9166c-127">-ResourceDefinition</span></span>
<span data-ttu-id="9166c-128">가상 컴퓨터 역할에 대 한 리소스 정의를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-128">Specifies a resource definition for the virtual machine role.</span></span>

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9166c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9166c-129">CommonParameters</span></span>
<span data-ttu-id="9166c-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9166c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9166c-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9166c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9166c-132">입력</span><span class="sxs-lookup"><span data-stu-id="9166c-132">INPUTS</span></span>

## <span data-ttu-id="9166c-133">출력</span><span class="sxs-lookup"><span data-stu-id="9166c-133">OUTPUTS</span></span>

## <span data-ttu-id="9166c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="9166c-134">NOTES</span></span>

## <span data-ttu-id="9166c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9166c-135">RELATED LINKS</span></span>

[<span data-ttu-id="9166c-136">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="9166c-136">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="9166c-137">제거-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="9166c-137">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="9166c-138">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="9166c-138">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


