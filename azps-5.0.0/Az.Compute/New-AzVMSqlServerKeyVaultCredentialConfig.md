---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215723"
---
# <span data-ttu-id="8cae0-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="8cae0-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="8cae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cae0-102">SYNOPSIS</span></span>
<span data-ttu-id="8cae0-103">가상 컴퓨터에서 SQL server 키 보관소 자격 증명에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cae0-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="8cae0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cae0-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cae0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8cae0-105">DESCRIPTION</span></span>

## <span data-ttu-id="8cae0-106">예제의</span><span class="sxs-lookup"><span data-stu-id="8cae0-106">EXAMPLES</span></span>

## <span data-ttu-id="8cae0-107">변수</span><span class="sxs-lookup"><span data-stu-id="8cae0-107">PARAMETERS</span></span>

### <span data-ttu-id="8cae0-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="8cae0-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="8cae0-109">Azure 키 자격 증명 모음 서비스 URL</span><span class="sxs-lookup"><span data-stu-id="8cae0-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="8cae0-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="8cae0-110">-CredentialName</span></span>
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

### <span data-ttu-id="8cae0-111">-사용</span><span class="sxs-lookup"><span data-stu-id="8cae0-111">-Enable</span></span>
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

### <span data-ttu-id="8cae0-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cae0-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8cae0-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8cae0-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="8cae0-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="8cae0-114">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="8cae0-115">-확인</span><span class="sxs-lookup"><span data-stu-id="8cae0-115">-Confirm</span></span>
<span data-ttu-id="8cae0-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cae0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cae0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cae0-117">-WhatIf</span></span>
<span data-ttu-id="8cae0-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8cae0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cae0-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cae0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cae0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cae0-120">CommonParameters</span></span>
<span data-ttu-id="8cae0-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cae0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cae0-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8cae0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cae0-123">입력</span><span class="sxs-lookup"><span data-stu-id="8cae0-123">INPUTS</span></span>

### <span data-ttu-id="8cae0-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8cae0-124">System.String</span></span>

### <span data-ttu-id="8cae0-125">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8cae0-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8cae0-126">System.webserver</span><span class="sxs-lookup"><span data-stu-id="8cae0-126">System.Security.SecureString</span></span>

## <span data-ttu-id="8cae0-127">출력</span><span class="sxs-lookup"><span data-stu-id="8cae0-127">OUTPUTS</span></span>

### <span data-ttu-id="8cae0-128">KeyVaultCredentialSettings를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cae0-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="8cae0-129">상속자</span><span class="sxs-lookup"><span data-stu-id="8cae0-129">NOTES</span></span>

## <span data-ttu-id="8cae0-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cae0-130">RELATED LINKS</span></span>
