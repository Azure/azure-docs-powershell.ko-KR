---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 12fe8cdc0e8e7210a2db7c7c6ccab1a0fcceeba3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056699"
---
# <span data-ttu-id="a2f28-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a2f28-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a2f28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2f28-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f28-103">키 보관소의 인증서 알림에 대해 등록 된 대화 상대를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="a2f28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2f28-104">SYNTAX</span></span>

### <span data-ttu-id="a2f28-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a2f28-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2f28-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a2f28-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2f28-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2f28-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2f28-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a2f28-108">DESCRIPTION</span></span>
<span data-ttu-id="a2f28-109">**AzKeyVaultCertificateContact** cmdlet은 키 보관소의 인증서 알림에 대해 등록 된 연락처를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="a2f28-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a2f28-110">EXAMPLES</span></span>

### <span data-ttu-id="a2f28-111">예제 1: 인증서 연락처 제거</span><span class="sxs-lookup"><span data-stu-id="a2f28-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="a2f28-112">이 명령은 Patti을 Contoso01 키 보관소의 인증서 연락처로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="a2f28-113">PassThru를 지정 하면 cmdlet은 나머지 인증서 연락처 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="a2f28-114">변수</span><span class="sxs-lookup"><span data-stu-id="a2f28-114">PARAMETERS</span></span>

### <span data-ttu-id="a2f28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f28-115">-DefaultProfile</span></span>
<span data-ttu-id="a2f28-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a2f28-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2f28-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a2f28-117">-EmailAddress</span></span>
<span data-ttu-id="a2f28-118">제거할 연락처의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="a2f28-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2f28-119">-InputObject</span></span>
<span data-ttu-id="a2f28-120">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="a2f28-120">KeyVault object.</span></span>

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

### <span data-ttu-id="a2f28-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2f28-121">-PassThru</span></span>
<span data-ttu-id="a2f28-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a2f28-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a2f28-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2f28-124">-ResourceId</span></span>
<span data-ttu-id="a2f28-125">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="a2f28-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a2f28-126">-VaultName</span></span>
<span data-ttu-id="a2f28-127">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a2f28-128">-확인</span><span class="sxs-lookup"><span data-stu-id="a2f28-128">-Confirm</span></span>
<span data-ttu-id="a2f28-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2f28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2f28-130">-WhatIf</span></span>
<span data-ttu-id="a2f28-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2f28-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2f28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f28-133">CommonParameters</span></span>
<span data-ttu-id="a2f28-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f28-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a2f28-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f28-136">입력</span><span class="sxs-lookup"><span data-stu-id="a2f28-136">INPUTS</span></span>

### <span data-ttu-id="a2f28-137">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a2f28-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a2f28-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a2f28-138">System.String</span></span>

## <span data-ttu-id="a2f28-139">출력</span><span class="sxs-lookup"><span data-stu-id="a2f28-139">OUTPUTS</span></span>

### <span data-ttu-id="a2f28-140">Microsoft. KeyVault. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a2f28-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a2f28-141">상속자</span><span class="sxs-lookup"><span data-stu-id="a2f28-141">NOTES</span></span>

## <span data-ttu-id="a2f28-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2f28-142">RELATED LINKS</span></span>

[<span data-ttu-id="a2f28-143">추가-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a2f28-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="a2f28-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a2f28-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

