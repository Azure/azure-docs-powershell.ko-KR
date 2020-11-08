---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047400"
---
# <span data-ttu-id="b0776-101">New-WAPackQuickVM</span><span class="sxs-lookup"><span data-stu-id="b0776-101">New-WAPackQuickVM</span></span>

## <span data-ttu-id="b0776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0776-102">SYNOPSIS</span></span>
<span data-ttu-id="b0776-103">템플릿을 기반으로 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-103">Creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="b0776-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0776-104">SYNTAX</span></span>

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b0776-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0776-105">DESCRIPTION</span></span>
<span data-ttu-id="b0776-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="b0776-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b0776-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b0776-109">**새-WAPackQuickVM** cmdlet은 템플릿을 기반으로 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-109">The **New-WAPackQuickVM** cmdlet creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="b0776-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b0776-110">EXAMPLES</span></span>

### <span data-ttu-id="b0776-111">예제 1: 템플릿을 기반으로 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="b0776-111">Example 1: Create a virtual machine based on a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

<span data-ttu-id="b0776-112">첫 번째 명령은 **PSCredential** 개체를 만든 다음 $Credentials 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-112">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="b0776-113">Cmdlet에서 계정과 암호를 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-113">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="b0776-114">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0776-114">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="b0776-115">두 번째 명령은 **WAPackVMTemplate** cmdlet을 사용 하 여 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-115">The second command gets a template by using the **Get-WAPackVMTemplate** cmdlet.</span></span>
<span data-ttu-id="b0776-116">명령은 서식 파일의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-116">The command specifies the ID of a template.</span></span>
<span data-ttu-id="b0776-117">명령이 $TemplateID 변수에 템플릿 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-117">The command stores the template object in the $TemplateID variable.</span></span>

<span data-ttu-id="b0776-118">마지막 명령은 VirtualMachine023 이라는 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-118">The final command creates a virtual machine named VirtualMachine023.</span></span>
<span data-ttu-id="b0776-119">명령은 $TemplateId에 저장 된 서식 파일의 가상 컴퓨터를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-119">The command bases the virtual machine on the template stored in $TemplateId.</span></span>

## <span data-ttu-id="b0776-120">변수</span><span class="sxs-lookup"><span data-stu-id="b0776-120">PARAMETERS</span></span>

### <span data-ttu-id="b0776-121">-이름</span><span class="sxs-lookup"><span data-stu-id="b0776-121">-Name</span></span>
<span data-ttu-id="b0776-122">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-122">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="b0776-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="b0776-123">-Profile</span></span>
<span data-ttu-id="b0776-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b0776-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b0776-126">-Template</span><span class="sxs-lookup"><span data-stu-id="b0776-126">-Template</span></span>
<span data-ttu-id="b0776-127">템플릿을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-127">Specifies a template.</span></span>
<span data-ttu-id="b0776-128">Cmdlet이 지정 된 템플릿을 기반으로 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-128">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="b0776-129">템플릿 개체를 가져오려면 **WAPackVMTemplate** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-129">To obtain a template object, use the **Get-WAPackVMTemplate** cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0776-130">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="b0776-130">-VMCredential</span></span>
<span data-ttu-id="b0776-131">로컬 관리자 계정에 대 한 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-131">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="b0776-132">**PSCredential** 개체를 가져오려면 **Get-Credential** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-132">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="b0776-133">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0776-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0776-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0776-134">CommonParameters</span></span>
<span data-ttu-id="b0776-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0776-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0776-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0776-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0776-137">입력</span><span class="sxs-lookup"><span data-stu-id="b0776-137">INPUTS</span></span>

## <span data-ttu-id="b0776-138">출력</span><span class="sxs-lookup"><span data-stu-id="b0776-138">OUTPUTS</span></span>

## <span data-ttu-id="b0776-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b0776-139">NOTES</span></span>

## <span data-ttu-id="b0776-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0776-140">RELATED LINKS</span></span>

[<span data-ttu-id="b0776-141">새-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="b0776-141">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="b0776-142">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="b0776-142">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)


