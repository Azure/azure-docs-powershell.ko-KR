---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: 30f88139bcd96f08dcb1c1263f5b5b5d1e35d4d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533784"
---
# <span data-ttu-id="c06e1-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c06e1-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="c06e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c06e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c06e1-103">자동화 자격 증명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c06e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c06e1-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c06e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c06e1-105">DESCRIPTION</span></span>
<span data-ttu-id="c06e1-106">**Set-AzureRmAutomationCredential** Cmdlet은 Azure Automation에서 자격 증명을 **PSCredential** 개체로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="c06e1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c06e1-107">EXAMPLES</span></span>

### <span data-ttu-id="c06e1-108">예제 1: 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="c06e1-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="c06e1-109">첫 번째 명령은 사용자 이름을 $User 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="c06e1-110">두 번째 명령은 ConvertTo-SecureString cmdlet을 사용 하 여 일반 텍스트 암호를 보안 문자열로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="c06e1-111">명령이 $Password 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="c06e1-112">세 번째 명령은 $User 및 $Password에 따라 자격 증명을 만든 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="c06e1-113">마지막 명령은 $Credential에서 자격 증명을 사용 하도록 ContosoCredential 이라는 자동화 자격 증명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="c06e1-114">변수</span><span class="sxs-lookup"><span data-stu-id="c06e1-114">PARAMETERS</span></span>

### <span data-ttu-id="c06e1-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c06e1-115">-AutomationAccountName</span></span>
<span data-ttu-id="c06e1-116">이 cmdlet이 자격 증명을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="c06e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06e1-117">-DefaultProfile</span></span>
<span data-ttu-id="c06e1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c06e1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c06e1-119">-설명</span><span class="sxs-lookup"><span data-stu-id="c06e1-119">-Description</span></span>
<span data-ttu-id="c06e1-120">이 cmdlet이 수정 하는 자격 증명에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c06e1-121">-이름</span><span class="sxs-lookup"><span data-stu-id="c06e1-121">-Name</span></span>
<span data-ttu-id="c06e1-122">이 cmdlet이 수정 하는 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c06e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c06e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="c06e1-124">이 cmdlet이 자격 증명을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="c06e1-125">-값</span><span class="sxs-lookup"><span data-stu-id="c06e1-125">-Value</span></span>
<span data-ttu-id="c06e1-126">자격 증명을 **PSCredential** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="c06e1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06e1-127">CommonParameters</span></span>
<span data-ttu-id="c06e1-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06e1-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c06e1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06e1-130">입력</span><span class="sxs-lookup"><span data-stu-id="c06e1-130">INPUTS</span></span>

### <span data-ttu-id="c06e1-131">않아야</span><span class="sxs-lookup"><span data-stu-id="c06e1-131">None</span></span>
<span data-ttu-id="c06e1-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c06e1-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c06e1-133">출력</span><span class="sxs-lookup"><span data-stu-id="c06e1-133">OUTPUTS</span></span>

### <span data-ttu-id="c06e1-134">Microsoft Azure.. m a. 모델-.pst 정보</span><span class="sxs-lookup"><span data-stu-id="c06e1-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="c06e1-135">상속자</span><span class="sxs-lookup"><span data-stu-id="c06e1-135">NOTES</span></span>

## <span data-ttu-id="c06e1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c06e1-136">RELATED LINKS</span></span>

[<span data-ttu-id="c06e1-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c06e1-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="c06e1-138">새로운 AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c06e1-138">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="c06e1-139">제거-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c06e1-139">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)


