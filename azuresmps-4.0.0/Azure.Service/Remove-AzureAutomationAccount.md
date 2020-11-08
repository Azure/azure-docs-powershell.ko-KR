---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B8E4F6BD-FBF2-4B19-AA61-02149F933ABB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52cba1ea3d42640693f2f330bf158a1eb078eebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046495"
---
# <span data-ttu-id="30ce8-101">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="30ce8-101">Remove-AzureAutomationAccount</span></span>

## <span data-ttu-id="30ce8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30ce8-102">SYNOPSIS</span></span>

<span data-ttu-id="30ce8-103">Automation 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce8-103">Removes an Automation Account.</span></span>

## <span data-ttu-id="30ce8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30ce8-104">SYNTAX</span></span>

```
Remove-AzureAutomationAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30ce8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30ce8-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="30ce8-106">**제거-AzureAutomationAccount** Cmdlet은 Microsoft Azure 자동화에서 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce8-106">The **Remove-AzureAutomationAccount** cmdlet removes an account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="30ce8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="30ce8-107">EXAMPLES</span></span>

### <span data-ttu-id="30ce8-108">예제 1: Automation 계정 제거</span><span class="sxs-lookup"><span data-stu-id="30ce8-108">Example 1: Remove an Automation account</span></span>
```
PS C:\> Remove-AzureAutomationAccount -Name "MyAutomationAccount" -Force
```

<span data-ttu-id="30ce8-109">이 명령은 사용자 유효성 검사를 묻지 않고 MyAutomationAccount 라는 이름의 Automation 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce8-109">This command removes an Automation account named MyAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="30ce8-110">변수</span><span class="sxs-lookup"><span data-stu-id="30ce8-110">PARAMETERS</span></span>

### <span data-ttu-id="30ce8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="30ce8-111">-Force</span></span>
<span data-ttu-id="30ce8-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce8-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ce8-113">-이름</span><span class="sxs-lookup"><span data-stu-id="30ce8-113">-Name</span></span>
<span data-ttu-id="30ce8-114">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce8-114">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="30ce8-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="30ce8-115">-Profile</span></span>
<span data-ttu-id="30ce8-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce8-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30ce8-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="30ce8-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30ce8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ce8-118">CommonParameters</span></span>
<span data-ttu-id="30ce8-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ce8-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ce8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ce8-121">입력</span><span class="sxs-lookup"><span data-stu-id="30ce8-121">INPUTS</span></span>

## <span data-ttu-id="30ce8-122">출력</span><span class="sxs-lookup"><span data-stu-id="30ce8-122">OUTPUTS</span></span>

## <span data-ttu-id="30ce8-123">상속자</span><span class="sxs-lookup"><span data-stu-id="30ce8-123">NOTES</span></span>

## <span data-ttu-id="30ce8-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30ce8-124">RELATED LINKS</span></span>

[<span data-ttu-id="30ce8-125">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="30ce8-125">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="30ce8-126">새-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="30ce8-126">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)


