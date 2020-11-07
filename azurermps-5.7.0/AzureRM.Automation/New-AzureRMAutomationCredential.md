---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: 59a1b7bc849767f8d7d389631a69ae1fc93dc759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704191"
---
# <span data-ttu-id="372cb-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="372cb-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="372cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="372cb-102">SYNOPSIS</span></span>
<span data-ttu-id="372cb-103">자동화 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="372cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="372cb-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="372cb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="372cb-105">DESCRIPTION</span></span>
<span data-ttu-id="372cb-106">**AzureRmAutomationCredential** Cmdlet은 Azure Automation에서 자격 증명을 **PSCredential** 개체로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="372cb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="372cb-107">EXAMPLES</span></span>

### <span data-ttu-id="372cb-108">예제 1: 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="372cb-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="372cb-109">첫 번째 명령은 사용자 이름을 $User 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="372cb-110">두 번째 명령은 ConvertTo-SecureString cmdlet을 사용 하 여 일반 텍스트 암호를 보안 문자열로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="372cb-111">명령이 $Password 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="372cb-112">세 번째 명령은 $User 및 $Password에 따라 자격 증명을 만든 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="372cb-113">마지막 명령은 $Credential를 사용 하는 ContosoCredential 이라는 자동화 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="372cb-114">변수</span><span class="sxs-lookup"><span data-stu-id="372cb-114">PARAMETERS</span></span>

### <span data-ttu-id="372cb-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="372cb-115">-AutomationAccountName</span></span>
<span data-ttu-id="372cb-116">이 cmdlet이 자격 증명을 저장 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372cb-117">-DefaultProfile</span></span>
<span data-ttu-id="372cb-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="372cb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372cb-119">-설명</span><span class="sxs-lookup"><span data-stu-id="372cb-119">-Description</span></span>
<span data-ttu-id="372cb-120">자격 증명에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="372cb-121">-이름</span><span class="sxs-lookup"><span data-stu-id="372cb-121">-Name</span></span>
<span data-ttu-id="372cb-122">자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-122">Specifies a name for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372cb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372cb-123">-ResourceGroupName</span></span>
<span data-ttu-id="372cb-124">이 cmdlet에서 자격 증명을 만드는 리소스 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372cb-125">-값</span><span class="sxs-lookup"><span data-stu-id="372cb-125">-Value</span></span>
<span data-ttu-id="372cb-126">자격 증명을 **PSCredential** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372cb-127">CommonParameters</span></span>
<span data-ttu-id="372cb-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372cb-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="372cb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372cb-130">입력</span><span class="sxs-lookup"><span data-stu-id="372cb-130">INPUTS</span></span>

### <span data-ttu-id="372cb-131">않아야</span><span class="sxs-lookup"><span data-stu-id="372cb-131">None</span></span>
<span data-ttu-id="372cb-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="372cb-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="372cb-133">출력</span><span class="sxs-lookup"><span data-stu-id="372cb-133">OUTPUTS</span></span>

### <span data-ttu-id="372cb-134">Microsoft Azure.. m a. 모델-.pst 정보</span><span class="sxs-lookup"><span data-stu-id="372cb-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="372cb-135">상속자</span><span class="sxs-lookup"><span data-stu-id="372cb-135">NOTES</span></span>

## <span data-ttu-id="372cb-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="372cb-136">RELATED LINKS</span></span>

[<span data-ttu-id="372cb-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="372cb-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="372cb-138">제거-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="372cb-138">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="372cb-139">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="372cb-139">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


