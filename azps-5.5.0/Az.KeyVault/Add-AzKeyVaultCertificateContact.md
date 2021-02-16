---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203871"
---
# <span data-ttu-id="b9480-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b9480-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="b9480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9480-102">SYNOPSIS</span></span>
<span data-ttu-id="b9480-103">인증서 알림에 대한 연락처를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="b9480-104">구문</span><span class="sxs-lookup"><span data-stu-id="b9480-104">SYNTAX</span></span>

### <span data-ttu-id="b9480-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="b9480-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9480-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="b9480-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9480-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9480-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9480-108">설명</span><span class="sxs-lookup"><span data-stu-id="b9480-108">DESCRIPTION</span></span>
<span data-ttu-id="b9480-109">**Add-AzKeyVaultCertificateContact** cmdlet은 Azure Key Vault의 인증서 알림에 대한 키 자격 증명 모음에 대한 연락처를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="b9480-110">연락처는 만료에 가까운 인증서, 갱신된 인증서 등의 이벤트에 대한 업데이트를 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="b9480-111">이러한 이벤트는 인증서 정책에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="b9480-112">예제</span><span class="sxs-lookup"><span data-stu-id="b9480-112">EXAMPLES</span></span>

### <span data-ttu-id="b9480-113">예제 1: 키 자격 증명 모음 인증서 연락처 추가</span><span class="sxs-lookup"><span data-stu-id="b9480-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="b9480-114">이 명령은 Patti Fuller를 ContosoKV01 키 자격 증명 모음에 대한 인증서 연락처로 추가하고 "ContosoKV01" 자격 증명 모음에 대한 연락처 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="b9480-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9480-115">PARAMETERS</span></span>

### <span data-ttu-id="b9480-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9480-116">-DefaultProfile</span></span>
<span data-ttu-id="b9480-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b9480-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9480-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b9480-118">-EmailAddress</span></span>
<span data-ttu-id="b9480-119">연락처의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="b9480-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9480-120">-InputObject</span></span>
<span data-ttu-id="b9480-121">KeyVault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-121">KeyVault object.</span></span>

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

### <span data-ttu-id="b9480-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9480-122">-PassThru</span></span>
<span data-ttu-id="b9480-123">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b9480-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b9480-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9480-125">-ResourceId</span></span>
<span data-ttu-id="b9480-126">KeyVault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="b9480-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b9480-127">-VaultName</span></span>
<span data-ttu-id="b9480-128">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9480-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9480-129">-Confirm</span></span>
<span data-ttu-id="b9480-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9480-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9480-131">-WhatIf</span></span>
<span data-ttu-id="b9480-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b9480-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9480-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9480-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9480-134">CommonParameters</span></span>
<span data-ttu-id="b9480-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9480-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9480-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b9480-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9480-137">입력</span><span class="sxs-lookup"><span data-stu-id="b9480-137">INPUTS</span></span>

### <span data-ttu-id="b9480-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b9480-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b9480-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b9480-139">System.String</span></span>

## <span data-ttu-id="b9480-140">출력</span><span class="sxs-lookup"><span data-stu-id="b9480-140">OUTPUTS</span></span>

### <span data-ttu-id="b9480-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b9480-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="b9480-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9480-142">NOTES</span></span>

## <span data-ttu-id="b9480-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9480-143">RELATED LINKS</span></span>

[<span data-ttu-id="b9480-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b9480-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="b9480-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b9480-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

