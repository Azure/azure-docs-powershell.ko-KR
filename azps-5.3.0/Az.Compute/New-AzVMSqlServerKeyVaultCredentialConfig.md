---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489271"
---
# <span data-ttu-id="ef65c-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="ef65c-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="ef65c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef65c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef65c-103">가상 머신에서 서버 SQL 자격 증명 모음 자격 증명에 대한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef65c-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="ef65c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef65c-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef65c-105">설명</span><span class="sxs-lookup"><span data-stu-id="ef65c-105">DESCRIPTION</span></span>

## <span data-ttu-id="ef65c-106">예제</span><span class="sxs-lookup"><span data-stu-id="ef65c-106">EXAMPLES</span></span>

## <span data-ttu-id="ef65c-107">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef65c-107">PARAMETERS</span></span>

### <span data-ttu-id="ef65c-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="ef65c-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="ef65c-109">Azure Key Vault 서비스 URL</span><span class="sxs-lookup"><span data-stu-id="ef65c-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="ef65c-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ef65c-110">-CredentialName</span></span>
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

### <span data-ttu-id="ef65c-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="ef65c-111">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef65c-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef65c-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ef65c-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ef65c-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="ef65c-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="ef65c-114">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef65c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef65c-115">-Confirm</span></span>
<span data-ttu-id="ef65c-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef65c-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef65c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef65c-117">-WhatIf</span></span>
<span data-ttu-id="ef65c-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ef65c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef65c-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef65c-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef65c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef65c-120">CommonParameters</span></span>
<span data-ttu-id="ef65c-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef65c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef65c-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ef65c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef65c-123">입력</span><span class="sxs-lookup"><span data-stu-id="ef65c-123">INPUTS</span></span>

### <span data-ttu-id="ef65c-124">System.String</span><span class="sxs-lookup"><span data-stu-id="ef65c-124">System.String</span></span>

### <span data-ttu-id="ef65c-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ef65c-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ef65c-126">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="ef65c-126">System.Security.SecureString</span></span>

## <span data-ttu-id="ef65c-127">출력</span><span class="sxs-lookup"><span data-stu-id="ef65c-127">OUTPUTS</span></span>

### <span data-ttu-id="ef65c-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="ef65c-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="ef65c-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef65c-129">NOTES</span></span>

## <span data-ttu-id="ef65c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef65c-130">RELATED LINKS</span></span>
