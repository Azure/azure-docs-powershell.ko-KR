---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9445B7FA-FC72-4F71-BD44-8AA55BE9BA0E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d2a3dbabb5bbe78ed571806aa69b9d79d4782b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045460"
---
# <span data-ttu-id="06dc8-101">Save-AzureServiceProjectPackage</span><span class="sxs-lookup"><span data-stu-id="06dc8-101">Save-AzureServiceProjectPackage</span></span>

## <span data-ttu-id="06dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="06dc8-103">서비스 프로젝트를 Azure 클라우드 패키지로 패키지 합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc8-103">Packages the service project into Azure cloud package.</span></span>

## <span data-ttu-id="06dc8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06dc8-104">SYNTAX</span></span>

```
Save-AzureServiceProjectPackage [-Local] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="06dc8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="06dc8-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="06dc8-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="06dc8-108">**저장-AzureServiceProjectPackage** cmdlet은 서비스 프로젝트를 Azure 클라우드 패키지 (\*. cspkg)에 패키지화 합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc8-108">The **Save-AzureServiceProjectPackage** cmdlet packages the service project into an Azure cloud package (\*.cspkg).</span></span>

## <span data-ttu-id="06dc8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="06dc8-109">EXAMPLES</span></span>

### <span data-ttu-id="06dc8-110">예제 1: 서비스 프로젝트 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="06dc8-110">Example 1: Create a service project package</span></span>
```
PS C:\> Save-AzureServiceProjectPackage
```

<span data-ttu-id="06dc8-111">이 예제에서는 MyAzureServiceProject 라는 서비스 프로젝트에 대 한 \* cspgk를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06dc8-111">This example creates a \*.cspgk for a service project named MyAzureServiceProject.</span></span>

## <span data-ttu-id="06dc8-112">변수</span><span class="sxs-lookup"><span data-stu-id="06dc8-112">PARAMETERS</span></span>

### <span data-ttu-id="06dc8-113">-로컬</span><span class="sxs-lookup"><span data-stu-id="06dc8-113">-Local</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06dc8-114">-프로필</span><span class="sxs-lookup"><span data-stu-id="06dc8-114">-Profile</span></span>
<span data-ttu-id="06dc8-115">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc8-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06dc8-116">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="06dc8-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06dc8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06dc8-117">CommonParameters</span></span>
<span data-ttu-id="06dc8-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06dc8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06dc8-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06dc8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06dc8-120">입력</span><span class="sxs-lookup"><span data-stu-id="06dc8-120">INPUTS</span></span>

## <span data-ttu-id="06dc8-121">출력</span><span class="sxs-lookup"><span data-stu-id="06dc8-121">OUTPUTS</span></span>

## <span data-ttu-id="06dc8-122">상속자</span><span class="sxs-lookup"><span data-stu-id="06dc8-122">NOTES</span></span>

## <span data-ttu-id="06dc8-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06dc8-123">RELATED LINKS</span></span>

[<span data-ttu-id="06dc8-124">게시-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="06dc8-124">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


