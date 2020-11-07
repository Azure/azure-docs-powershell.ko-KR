---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: 7b41b5eaaf0fae38b8cb4e9043b83889e516f93b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697739"
---
# <span data-ttu-id="65900-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="65900-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="65900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65900-102">SYNOPSIS</span></span>
<span data-ttu-id="65900-103">자동화 자격 증명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="65900-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65900-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65900-105">설명은</span><span class="sxs-lookup"><span data-stu-id="65900-105">DESCRIPTION</span></span>
<span data-ttu-id="65900-106">**Set-AzAutomationCredential** Cmdlet은 Azure Automation에서 자격 증명을 **PSCredential** 개체로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="65900-107">예제의</span><span class="sxs-lookup"><span data-stu-id="65900-107">EXAMPLES</span></span>

### <span data-ttu-id="65900-108">예제 1: 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="65900-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="65900-109">첫 번째 명령은 사용자 이름을 $User 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="65900-110">두 번째 명령은 ConvertTo-SecureString cmdlet을 사용 하 여 일반 텍스트 암호를 보안 문자열로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="65900-111">명령이 $Password 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="65900-112">세 번째 명령은 $User 및 $Password에 따라 자격 증명을 만든 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="65900-113">마지막 명령은 $Credential에서 자격 증명을 사용 하도록 ContosoCredential 이라는 자동화 자격 증명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="65900-114">변수</span><span class="sxs-lookup"><span data-stu-id="65900-114">PARAMETERS</span></span>

### <span data-ttu-id="65900-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65900-115">-AutomationAccountName</span></span>
<span data-ttu-id="65900-116">이 cmdlet이 자격 증명을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65900-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65900-117">-DefaultProfile</span></span>
<span data-ttu-id="65900-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="65900-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65900-119">-설명</span><span class="sxs-lookup"><span data-stu-id="65900-119">-Description</span></span>
<span data-ttu-id="65900-120">이 cmdlet이 수정 하는 자격 증명에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65900-121">-이름</span><span class="sxs-lookup"><span data-stu-id="65900-121">-Name</span></span>
<span data-ttu-id="65900-122">이 cmdlet이 수정 하는 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65900-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65900-123">-ResourceGroupName</span></span>
<span data-ttu-id="65900-124">이 cmdlet이 자격 증명을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65900-125">-값</span><span class="sxs-lookup"><span data-stu-id="65900-125">-Value</span></span>
<span data-ttu-id="65900-126">자격 증명을 **PSCredential** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65900-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65900-127">CommonParameters</span></span>
<span data-ttu-id="65900-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65900-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65900-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65900-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65900-130">입력</span><span class="sxs-lookup"><span data-stu-id="65900-130">INPUTS</span></span>

### <span data-ttu-id="65900-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="65900-131">System.String</span></span>

### <span data-ttu-id="65900-132">System.webserver. PSCredential</span><span class="sxs-lookup"><span data-stu-id="65900-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="65900-133">출력</span><span class="sxs-lookup"><span data-stu-id="65900-133">OUTPUTS</span></span>

### <span data-ttu-id="65900-134">Microsoft Azure.. m a. 모델-.pst 정보</span><span class="sxs-lookup"><span data-stu-id="65900-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="65900-135">상속자</span><span class="sxs-lookup"><span data-stu-id="65900-135">NOTES</span></span>

## <span data-ttu-id="65900-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65900-136">RELATED LINKS</span></span>

[<span data-ttu-id="65900-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="65900-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="65900-138">새로운 AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="65900-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="65900-139">제거-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="65900-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

