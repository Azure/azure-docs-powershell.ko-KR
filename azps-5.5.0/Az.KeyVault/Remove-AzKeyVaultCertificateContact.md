---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 12fe8cdc0e8e7210a2db7c7c6ccab1a0fcceeba3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199988"
---
# <span data-ttu-id="b2ee3-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b2ee3-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="b2ee3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ee3-103">키 자격 증명 모음에서 인증서 알림에 등록된 연락처를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="b2ee3-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2ee3-104">SYNTAX</span></span>

### <span data-ttu-id="b2ee3-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b2ee3-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2ee3-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="b2ee3-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2ee3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2ee3-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2ee3-108">설명</span><span class="sxs-lookup"><span data-stu-id="b2ee3-108">DESCRIPTION</span></span>
<span data-ttu-id="b2ee3-109">**Remove-AzKeyVaultCertificateContact** cmdlet은 키 자격 증명 모음에서 인증서 알림에 등록된 연락처를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="b2ee3-110">예제</span><span class="sxs-lookup"><span data-stu-id="b2ee3-110">EXAMPLES</span></span>

### <span data-ttu-id="b2ee3-111">예제 1: 인증서 연락처 제거</span><span class="sxs-lookup"><span data-stu-id="b2ee3-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="b2ee3-112">이 명령은 Contoso01 키 자격 증명 모음에 대한 인증서 연락처로 Patti Fuller를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="b2ee3-113">PassThru를 지정하면 cmdlet은 나머지 인증서 연락처 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="b2ee3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2ee3-114">PARAMETERS</span></span>

### <span data-ttu-id="b2ee3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ee3-115">-DefaultProfile</span></span>
<span data-ttu-id="b2ee3-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b2ee3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2ee3-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b2ee3-117">-EmailAddress</span></span>
<span data-ttu-id="b2ee3-118">제거할 연락처의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="b2ee3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2ee3-119">-InputObject</span></span>
<span data-ttu-id="b2ee3-120">KeyVault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-120">KeyVault object.</span></span>

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

### <span data-ttu-id="b2ee3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2ee3-121">-PassThru</span></span>
<span data-ttu-id="b2ee3-122">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b2ee3-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b2ee3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2ee3-124">-ResourceId</span></span>
<span data-ttu-id="b2ee3-125">KeyVault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="b2ee3-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b2ee3-126">-VaultName</span></span>
<span data-ttu-id="b2ee3-127">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="b2ee3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2ee3-128">-Confirm</span></span>
<span data-ttu-id="b2ee3-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2ee3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2ee3-130">-WhatIf</span></span>
<span data-ttu-id="b2ee3-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b2ee3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2ee3-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2ee3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ee3-133">CommonParameters</span></span>
<span data-ttu-id="b2ee3-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2ee3-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b2ee3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ee3-136">입력</span><span class="sxs-lookup"><span data-stu-id="b2ee3-136">INPUTS</span></span>

### <span data-ttu-id="b2ee3-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b2ee3-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b2ee3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b2ee3-138">System.String</span></span>

## <span data-ttu-id="b2ee3-139">출력</span><span class="sxs-lookup"><span data-stu-id="b2ee3-139">OUTPUTS</span></span>

### <span data-ttu-id="b2ee3-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b2ee3-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="b2ee3-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2ee3-141">NOTES</span></span>

## <span data-ttu-id="b2ee3-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2ee3-142">RELATED LINKS</span></span>

[<span data-ttu-id="b2ee3-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b2ee3-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="b2ee3-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b2ee3-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

