---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 59CDE74B-EFB3-4904-A482-466B0EA17F4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a787193669cab32a43b7c9b9eb2010a6e545539b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046224"
---
# <span data-ttu-id="e6743-101">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e6743-101">New-AzureAutomationAccount</span></span>

## <span data-ttu-id="e6743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6743-102">SYNOPSIS</span></span>

<span data-ttu-id="e6743-103">Automation 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6743-103">Creates an Automation account.</span></span>

## <span data-ttu-id="e6743-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6743-104">SYNTAX</span></span>

```
New-AzureAutomationAccount -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6743-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e6743-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e6743-106">**새로운-AzureAutomationAccount** Cmdlet은 Microsoft Azure 자동화에 새 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6743-106">The **New-AzureAutomationAccount** cmdlet creates a new account in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="e6743-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e6743-107">EXAMPLES</span></span>

### <span data-ttu-id="e6743-108">예제 1: Automation 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="e6743-108">Example 1: Create an Automation account</span></span>
```
PS C:\> New-AzureAutomationAccount -Name "MyAutomationAccount" -Location "East US"
```

<span data-ttu-id="e6743-109">이 명령은 동부 US 지역에 MyAutomationAccount 라는 자동화 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6743-109">This command creates an Automation account named MyAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="e6743-110">변수</span><span class="sxs-lookup"><span data-stu-id="e6743-110">PARAMETERS</span></span>

### <span data-ttu-id="e6743-111">-위치</span><span class="sxs-lookup"><span data-stu-id="e6743-111">-Location</span></span>
<span data-ttu-id="e6743-112">계정 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6743-112">Specifies the location of the account.</span></span>

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

### <span data-ttu-id="e6743-113">-이름</span><span class="sxs-lookup"><span data-stu-id="e6743-113">-Name</span></span>
<span data-ttu-id="e6743-114">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6743-114">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6743-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="e6743-115">-Profile</span></span>
<span data-ttu-id="e6743-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6743-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6743-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e6743-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6743-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6743-118">CommonParameters</span></span>
<span data-ttu-id="e6743-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6743-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6743-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6743-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6743-121">입력</span><span class="sxs-lookup"><span data-stu-id="e6743-121">INPUTS</span></span>

## <span data-ttu-id="e6743-122">출력</span><span class="sxs-lookup"><span data-stu-id="e6743-122">OUTPUTS</span></span>

### <span data-ttu-id="e6743-123">Microsoft Azure. \*.</span><span class="sxs-lookup"><span data-stu-id="e6743-123">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e6743-124">상속자</span><span class="sxs-lookup"><span data-stu-id="e6743-124">NOTES</span></span>

## <span data-ttu-id="e6743-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6743-125">RELATED LINKS</span></span>

[<span data-ttu-id="e6743-126">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e6743-126">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="e6743-127">-AzureAutomationAccount 제거</span><span class="sxs-lookup"><span data-stu-id="e6743-127">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


