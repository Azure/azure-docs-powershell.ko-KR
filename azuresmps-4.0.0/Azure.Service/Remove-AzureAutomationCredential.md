---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4D87DD30-4AEF-4269-93B2-AE5964334AC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b581712f020b8168c052634e0f20244e16a7d950
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046480"
---
# <span data-ttu-id="3a355-101">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3a355-101">Remove-AzureAutomationCredential</span></span>

## <span data-ttu-id="3a355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a355-102">SYNOPSIS</span></span>

<span data-ttu-id="3a355-103">자동화에서 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a355-103">Removes a credential from Automation.</span></span>

## <span data-ttu-id="3a355-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a355-104">SYNTAX</span></span>

```
Remove-AzureAutomationCredential -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a355-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3a355-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3a355-106">**제거-AzureAutomationCredential** Cmdlet은 Microsoft Azure 자동화에서 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a355-106">The **Remove-AzureAutomationCredential** cmdlet removes a credential from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="3a355-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3a355-107">EXAMPLES</span></span>

### <span data-ttu-id="3a355-108">예제 1: 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="3a355-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="3a355-109">이 명령은 Contoso17 이라는 자동화 계정에서 MyCredential 이라는 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a355-109">This command removes a credential named MyCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3a355-110">변수</span><span class="sxs-lookup"><span data-stu-id="3a355-110">PARAMETERS</span></span>

### <span data-ttu-id="3a355-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a355-111">-AutomationAccountName</span></span>
<span data-ttu-id="3a355-112">자격 증명을 사용 하 여 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a355-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="3a355-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3a355-113">-Force</span></span>
<span data-ttu-id="3a355-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a355-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a355-115">-이름</span><span class="sxs-lookup"><span data-stu-id="3a355-115">-Name</span></span>
<span data-ttu-id="3a355-116">제거할 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a355-116">Specifies the name of the credential to remove.</span></span>

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

### <span data-ttu-id="3a355-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="3a355-117">-Profile</span></span>
<span data-ttu-id="3a355-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a355-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a355-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3a355-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a355-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a355-120">CommonParameters</span></span>
<span data-ttu-id="3a355-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a355-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a355-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a355-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a355-123">입력</span><span class="sxs-lookup"><span data-stu-id="3a355-123">INPUTS</span></span>

## <span data-ttu-id="3a355-124">출력</span><span class="sxs-lookup"><span data-stu-id="3a355-124">OUTPUTS</span></span>

## <span data-ttu-id="3a355-125">상속자</span><span class="sxs-lookup"><span data-stu-id="3a355-125">NOTES</span></span>

## <span data-ttu-id="3a355-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a355-126">RELATED LINKS</span></span>

[<span data-ttu-id="3a355-127">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3a355-127">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="3a355-128">새-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3a355-128">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="3a355-129">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3a355-129">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


