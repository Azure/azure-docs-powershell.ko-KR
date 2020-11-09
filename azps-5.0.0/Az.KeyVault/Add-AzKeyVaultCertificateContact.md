---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304634"
---
# <span data-ttu-id="70c2f-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="70c2f-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="70c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="70c2f-103">인증서 알림에 대 한 대화 상대를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="70c2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70c2f-104">SYNTAX</span></span>

### <span data-ttu-id="70c2f-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="70c2f-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c2f-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="70c2f-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c2f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="70c2f-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70c2f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="70c2f-108">DESCRIPTION</span></span>
<span data-ttu-id="70c2f-109">**AzKeyVaultCertificateContact** Cmdlet은 Azure key vault의 인증서 알림 용 키 보관소에 대 한 연락처를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="70c2f-110">연락처가 만료, 인증서 갱신 등의 인증서와 같은 이벤트에 대 한 업데이트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="70c2f-111">이러한 이벤트는 인증서 정책에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="70c2f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="70c2f-112">EXAMPLES</span></span>

### <span data-ttu-id="70c2f-113">예제 1: 주요 자격 증명 모음 인증서 연락처 추가</span><span class="sxs-lookup"><span data-stu-id="70c2f-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="70c2f-114">이 명령은 Patti을 ContosoKV01 키 보관소에 대 한 인증서 연락처로 추가 하 고 "ContosoKV01" 볼트에 대 한 연락처 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="70c2f-115">변수</span><span class="sxs-lookup"><span data-stu-id="70c2f-115">PARAMETERS</span></span>

### <span data-ttu-id="70c2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c2f-116">-DefaultProfile</span></span>
<span data-ttu-id="70c2f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="70c2f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70c2f-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="70c2f-118">-EmailAddress</span></span>
<span data-ttu-id="70c2f-119">연락처의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="70c2f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70c2f-120">-InputObject</span></span>
<span data-ttu-id="70c2f-121">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="70c2f-121">KeyVault object.</span></span>

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

### <span data-ttu-id="70c2f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70c2f-122">-PassThru</span></span>
<span data-ttu-id="70c2f-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="70c2f-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="70c2f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70c2f-125">-ResourceId</span></span>
<span data-ttu-id="70c2f-126">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="70c2f-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="70c2f-127">-VaultName</span></span>
<span data-ttu-id="70c2f-128">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="70c2f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="70c2f-129">-Confirm</span></span>
<span data-ttu-id="70c2f-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c2f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c2f-131">-WhatIf</span></span>
<span data-ttu-id="70c2f-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c2f-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c2f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c2f-134">CommonParameters</span></span>
<span data-ttu-id="70c2f-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70c2f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c2f-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70c2f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c2f-137">입력</span><span class="sxs-lookup"><span data-stu-id="70c2f-137">INPUTS</span></span>

### <span data-ttu-id="70c2f-138">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="70c2f-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="70c2f-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="70c2f-139">System.String</span></span>

## <span data-ttu-id="70c2f-140">출력</span><span class="sxs-lookup"><span data-stu-id="70c2f-140">OUTPUTS</span></span>

### <span data-ttu-id="70c2f-141">Microsoft. KeyVault. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="70c2f-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="70c2f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="70c2f-142">NOTES</span></span>

## <span data-ttu-id="70c2f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70c2f-143">RELATED LINKS</span></span>

[<span data-ttu-id="70c2f-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="70c2f-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="70c2f-145">제거-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="70c2f-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

