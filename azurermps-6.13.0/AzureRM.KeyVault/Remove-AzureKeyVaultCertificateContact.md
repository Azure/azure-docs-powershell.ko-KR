---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: aee18adf3530976af4b17ffa15f94624248a7db7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530274"
---
# <span data-ttu-id="bc078-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bc078-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="bc078-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc078-102">SYNOPSIS</span></span>
<span data-ttu-id="bc078-103">키 보관소의 인증서 알림에 대해 등록 된 대화 상대를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc078-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc078-104">SYNTAX</span></span>

### <span data-ttu-id="bc078-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="bc078-105">ByName (Default)</span></span>
```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc078-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="bc078-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc078-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc078-107">ByResourceId</span></span>
```
Remove-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc078-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bc078-108">DESCRIPTION</span></span>
<span data-ttu-id="bc078-109">**AzureKeyVaultCertificateContact** cmdlet은 키 보관소의 인증서 알림에 대해 등록 된 연락처를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-109">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="bc078-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bc078-110">EXAMPLES</span></span>

### <span data-ttu-id="bc078-111">예제 1: 인증서 연락처 제거</span><span class="sxs-lookup"><span data-stu-id="bc078-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="bc078-112">이 명령은 Patti을 Contoso01 키 보관소의 인증서 연락처로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="bc078-113">PassThru를 지정 하면 cmdlet은 나머지 인증서 연락처 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="bc078-114">변수</span><span class="sxs-lookup"><span data-stu-id="bc078-114">PARAMETERS</span></span>

### <span data-ttu-id="bc078-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc078-115">-DefaultProfile</span></span>
<span data-ttu-id="bc078-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bc078-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc078-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="bc078-117">-EmailAddress</span></span>
<span data-ttu-id="bc078-118">제거할 연락처의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-118">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc078-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc078-119">-InputObject</span></span>
<span data-ttu-id="bc078-120">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="bc078-120">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc078-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc078-121">-PassThru</span></span>
<span data-ttu-id="bc078-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bc078-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc078-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc078-124">-ResourceId</span></span>
<span data-ttu-id="bc078-125">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-125">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc078-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bc078-126">-VaultName</span></span>
<span data-ttu-id="bc078-127">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc078-128">-확인</span><span class="sxs-lookup"><span data-stu-id="bc078-128">-Confirm</span></span>
<span data-ttu-id="bc078-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc078-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc078-130">-WhatIf</span></span>
<span data-ttu-id="bc078-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc078-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc078-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc078-133">CommonParameters</span></span>
<span data-ttu-id="bc078-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc078-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc078-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc078-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc078-136">입력</span><span class="sxs-lookup"><span data-stu-id="bc078-136">INPUTS</span></span>

### <span data-ttu-id="bc078-137">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bc078-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="bc078-138">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc078-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="bc078-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bc078-139">System.String</span></span>

## <span data-ttu-id="bc078-140">출력</span><span class="sxs-lookup"><span data-stu-id="bc078-140">OUTPUTS</span></span>

### <span data-ttu-id="bc078-141">Microsoft. KeyVault. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bc078-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="bc078-142">상속자</span><span class="sxs-lookup"><span data-stu-id="bc078-142">NOTES</span></span>

## <span data-ttu-id="bc078-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc078-143">RELATED LINKS</span></span>

[<span data-ttu-id="bc078-144">추가-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bc078-144">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="bc078-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bc078-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

