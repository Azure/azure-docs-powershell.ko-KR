---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 7cf5070b6f03c7bc19b8d05991314569616c06ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970720"
---
# <span data-ttu-id="cd433-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cd433-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="cd433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd433-102">SYNOPSIS</span></span>
<span data-ttu-id="cd433-103">인증서 알림에 대한 연락처를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="cd433-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd433-104">SYNTAX</span></span>

### <span data-ttu-id="cd433-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="cd433-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd433-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="cd433-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd433-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd433-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd433-108">설명</span><span class="sxs-lookup"><span data-stu-id="cd433-108">DESCRIPTION</span></span>
<span data-ttu-id="cd433-109">**Add-AzKeyVaultCertificateContact** cmdlet은 Azure Key Vault의 인증서 알림에 대한 키 자격 증명 모음에 대한 연락처를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="cd433-110">연락처는 만료에 가까운 인증서, 인증서 갱신 등의 이벤트에 대한 업데이트를 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="cd433-111">이러한 이벤트는 인증서 정책에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="cd433-112">예제</span><span class="sxs-lookup"><span data-stu-id="cd433-112">EXAMPLES</span></span>

### <span data-ttu-id="cd433-113">예제 1: 키 자격 증명 모음 인증서 연락처 추가</span><span class="sxs-lookup"><span data-stu-id="cd433-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="cd433-114">이 명령은 ContosoKV01 키 자격 증명 모음에 대한 인증서 연락처로 Patti Fuller를 추가하고 "ContosoKV01" 자격 증명 모음에 대한 연락처 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="cd433-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cd433-115">PARAMETERS</span></span>

### <span data-ttu-id="cd433-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd433-116">-DefaultProfile</span></span>
<span data-ttu-id="cd433-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cd433-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd433-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="cd433-118">-EmailAddress</span></span>
<span data-ttu-id="cd433-119">연락처의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="cd433-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd433-120">-InputObject</span></span>
<span data-ttu-id="cd433-121">KeyVault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-121">KeyVault object.</span></span>

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

### <span data-ttu-id="cd433-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd433-122">-PassThru</span></span>
<span data-ttu-id="cd433-123">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd433-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd433-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd433-125">-ResourceId</span></span>
<span data-ttu-id="cd433-126">KeyVault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="cd433-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cd433-127">-VaultName</span></span>
<span data-ttu-id="cd433-128">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="cd433-129">-확인</span><span class="sxs-lookup"><span data-stu-id="cd433-129">-Confirm</span></span>
<span data-ttu-id="cd433-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd433-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd433-131">-WhatIf</span></span>
<span data-ttu-id="cd433-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd433-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd433-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd433-134">CommonParameters</span></span>
<span data-ttu-id="cd433-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd433-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd433-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd433-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd433-137">입력</span><span class="sxs-lookup"><span data-stu-id="cd433-137">INPUTS</span></span>

### <span data-ttu-id="cd433-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cd433-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="cd433-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cd433-139">System.String</span></span>

## <span data-ttu-id="cd433-140">출력</span><span class="sxs-lookup"><span data-stu-id="cd433-140">OUTPUTS</span></span>

### <span data-ttu-id="cd433-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cd433-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="cd433-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd433-142">NOTES</span></span>

## <span data-ttu-id="cd433-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd433-143">RELATED LINKS</span></span>

[<span data-ttu-id="cd433-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cd433-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="cd433-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cd433-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

