---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: d9f732a40b61687d7970fdf24f9f9f0f841b2cc7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876993"
---
# <span data-ttu-id="58041-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="58041-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="58041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58041-102">SYNOPSIS</span></span>
<span data-ttu-id="58041-103">가상 컴퓨터에서 SQL server 키 보관소 자격 증명에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58041-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="58041-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58041-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58041-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58041-105">DESCRIPTION</span></span>

## <span data-ttu-id="58041-106">예제의</span><span class="sxs-lookup"><span data-stu-id="58041-106">EXAMPLES</span></span>

## <span data-ttu-id="58041-107">변수</span><span class="sxs-lookup"><span data-stu-id="58041-107">PARAMETERS</span></span>

### <span data-ttu-id="58041-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="58041-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="58041-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="58041-109">-CredentialName</span></span>
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

### <span data-ttu-id="58041-110">-사용</span><span class="sxs-lookup"><span data-stu-id="58041-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58041-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58041-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="58041-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="58041-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="58041-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="58041-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58041-114">-확인</span><span class="sxs-lookup"><span data-stu-id="58041-114">-Confirm</span></span>
<span data-ttu-id="58041-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58041-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58041-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58041-116">-WhatIf</span></span>
<span data-ttu-id="58041-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58041-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="58041-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58041-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58041-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58041-119">CommonParameters</span></span>
<span data-ttu-id="58041-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58041-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58041-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58041-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58041-122">입력</span><span class="sxs-lookup"><span data-stu-id="58041-122">INPUTS</span></span>

### <span data-ttu-id="58041-123">않아야</span><span class="sxs-lookup"><span data-stu-id="58041-123">None</span></span>
<span data-ttu-id="58041-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58041-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58041-125">출력</span><span class="sxs-lookup"><span data-stu-id="58041-125">OUTPUTS</span></span>

### <span data-ttu-id="58041-126">KeyVaultCredentialSettings를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="58041-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="58041-127">상속자</span><span class="sxs-lookup"><span data-stu-id="58041-127">NOTES</span></span>

## <span data-ttu-id="58041-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58041-128">RELATED LINKS</span></span>

