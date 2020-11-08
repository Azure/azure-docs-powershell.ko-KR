---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C92B4B70-4342-4219-80D3-FB79BDC171A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16fbdf1a0a63fb5a75aa7bc200036a7332ea15f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045831"
---
# <span data-ttu-id="7cc7d-101">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7cc7d-101">Set-AzureAutomationCredential</span></span>

## <span data-ttu-id="7cc7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cc7d-102">SYNOPSIS</span></span>

<span data-ttu-id="7cc7d-103">자동화의 자격 증명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-103">Modifies a credential in Automation.</span></span>

## <span data-ttu-id="7cc7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7cc7d-104">SYNTAX</span></span>

```
Set-AzureAutomationCredential -Name <String> [-Description <String>] [-Value <PSCredential>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7cc7d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7cc7d-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7cc7d-106">**Set AzureAutomationCredential** Cmdlet은 Microsoft Azure Automation에서 자격 증명을 **PSCredential** 개체로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-106">The **Set-AzureAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="7cc7d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7cc7d-107">EXAMPLES</span></span>

### <span data-ttu-id="7cc7d-108">예제 1: 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="7cc7d-108">Example 1: Update a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contos17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="7cc7d-109">이러한 명령은 MyCredential 이라는 기존 자격 증명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-109">These commands update an existing credential named MyCredential.</span></span>
<span data-ttu-id="7cc7d-110">사용자 이름 및 암호를 포함 하는 자격 증명 개체가 먼저 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="7cc7d-111">그런 다음 마지막 명령에서 자동화 자격 증명을 업데이트 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-111">This is then used in the last command to update the automation credential.</span></span>

## <span data-ttu-id="7cc7d-112">변수</span><span class="sxs-lookup"><span data-stu-id="7cc7d-112">PARAMETERS</span></span>

### <span data-ttu-id="7cc7d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7cc7d-113">-AutomationAccountName</span></span>
<span data-ttu-id="7cc7d-114">자격 증명을 사용 하 여 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-114">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="7cc7d-115">-설명</span><span class="sxs-lookup"><span data-stu-id="7cc7d-115">-Description</span></span>
<span data-ttu-id="7cc7d-116">자격 증명에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="7cc7d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="7cc7d-117">-Name</span></span>
<span data-ttu-id="7cc7d-118">자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-118">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="7cc7d-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="7cc7d-119">-Profile</span></span>
<span data-ttu-id="7cc7d-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7cc7d-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7cc7d-122">-값</span><span class="sxs-lookup"><span data-stu-id="7cc7d-122">-Value</span></span>
<span data-ttu-id="7cc7d-123">자격 증명을 **PSCredential** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc7d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc7d-124">CommonParameters</span></span>
<span data-ttu-id="7cc7d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc7d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc7d-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc7d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc7d-127">입력</span><span class="sxs-lookup"><span data-stu-id="7cc7d-127">INPUTS</span></span>

## <span data-ttu-id="7cc7d-128">출력</span><span class="sxs-lookup"><span data-stu-id="7cc7d-128">OUTPUTS</span></span>

### <span data-ttu-id="7cc7d-129">Microsoft Azure.. m a. 모델-.pst 정보</span><span class="sxs-lookup"><span data-stu-id="7cc7d-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="7cc7d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="7cc7d-130">NOTES</span></span>

## <span data-ttu-id="7cc7d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cc7d-131">RELATED LINKS</span></span>

[<span data-ttu-id="7cc7d-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7cc7d-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="7cc7d-133">새-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7cc7d-133">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="7cc7d-134">-AzureAutomationCredential 제거</span><span class="sxs-lookup"><span data-stu-id="7cc7d-134">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)


