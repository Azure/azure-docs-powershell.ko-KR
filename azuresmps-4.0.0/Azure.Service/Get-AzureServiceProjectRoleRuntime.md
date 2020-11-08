---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CEFFEF9F-4500-447E-99F1-FE053AED880A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e5b65a88e41ce08ec1d60bc140828963950f447
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045598"
---
# <span data-ttu-id="7b197-101">Get-AzureServiceProjectRoleRuntime</span><span class="sxs-lookup"><span data-stu-id="7b197-101">Get-AzureServiceProjectRoleRuntime</span></span>

## <span data-ttu-id="7b197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b197-102">SYNOPSIS</span></span>
<span data-ttu-id="7b197-103">역할에 설치 하는 데 사용할 수 있는 런타임을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b197-103">Get the runtimes available to install in a role.</span></span>

## <span data-ttu-id="7b197-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b197-104">SYNTAX</span></span>

```
Get-AzureServiceProjectRoleRuntime [-Runtime <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7b197-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7b197-105">DESCRIPTION</span></span>
<span data-ttu-id="7b197-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b197-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7b197-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b197-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7b197-108">역할에 설치 하는 데 사용할 수 있는 런타임을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b197-108">Gets the runtimes available to install in a role.</span></span>

## <span data-ttu-id="7b197-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7b197-109">EXAMPLES</span></span>

## <span data-ttu-id="7b197-110">변수</span><span class="sxs-lookup"><span data-stu-id="7b197-110">PARAMETERS</span></span>

### <span data-ttu-id="7b197-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="7b197-111">-Profile</span></span>
<span data-ttu-id="7b197-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b197-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7b197-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7b197-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7b197-114">런타임</span><span class="sxs-lookup"><span data-stu-id="7b197-114">-Runtime</span></span>
<span data-ttu-id="7b197-115">런타임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b197-115">The name of the runtime.</span></span>
<span data-ttu-id="7b197-116">런타임이 지정 된 경우 Windows Azure의 역할에 설치 하는 데 사용할 수 있는 해당 런타임의 특정 버전만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b197-116">If a runtime specified, only the specific versions of that runtime available to install in your role in Windows Azure will be returned.</span></span>

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

### <span data-ttu-id="7b197-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b197-117">CommonParameters</span></span>
<span data-ttu-id="7b197-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b197-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b197-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b197-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b197-120">입력</span><span class="sxs-lookup"><span data-stu-id="7b197-120">INPUTS</span></span>

## <span data-ttu-id="7b197-121">출력</span><span class="sxs-lookup"><span data-stu-id="7b197-121">OUTPUTS</span></span>

## <span data-ttu-id="7b197-122">상속자</span><span class="sxs-lookup"><span data-stu-id="7b197-122">NOTES</span></span>

## <span data-ttu-id="7b197-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b197-123">RELATED LINKS</span></span>

[<span data-ttu-id="7b197-124">추가-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="7b197-124">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="7b197-125">추가-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="7b197-125">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="7b197-126">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="7b197-126">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)

[<span data-ttu-id="7b197-127">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="7b197-127">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


