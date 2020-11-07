---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: d6a06c3f4c50e10522ed06e6b1cd4185c1ef6768
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699059"
---
# <span data-ttu-id="4576e-101">Disable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4576e-101">Disable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="4576e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4576e-102">SYNOPSIS</span></span>
<span data-ttu-id="4576e-103">서버에서 고급 위협 방지를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4576e-103">Disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="4576e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4576e-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4576e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4576e-105">DESCRIPTION</span></span>
<span data-ttu-id="4576e-106">**AzSqlServerAdvancedThreatProtection** cmdlet은 서버에서 고급 위협 방지를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4576e-106">The **Disable-AzSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="4576e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4576e-107">EXAMPLES</span></span>

### <span data-ttu-id="4576e-108">예제 1-서버 고급 위협 방지 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="4576e-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="4576e-109">예제 2-서버 리소스에서 서버 고급 위협 방지를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="4576e-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="4576e-110">변수</span><span class="sxs-lookup"><span data-stu-id="4576e-110">PARAMETERS</span></span>

### <span data-ttu-id="4576e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4576e-111">-DefaultProfile</span></span>
<span data-ttu-id="4576e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4576e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4576e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4576e-113">-InputObject</span></span>
<span data-ttu-id="4576e-114">고급 위협 보호 정책 작업에 사용할 서버 개체</span><span class="sxs-lookup"><span data-stu-id="4576e-114">The server object to use with Advanced Threat Protection policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4576e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4576e-115">-ResourceGroupName</span></span>
<span data-ttu-id="4576e-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4576e-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="4576e-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4576e-117">-ServerName</span></span>
<span data-ttu-id="4576e-118">SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4576e-118">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4576e-119">-확인</span><span class="sxs-lookup"><span data-stu-id="4576e-119">-Confirm</span></span>
<span data-ttu-id="4576e-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4576e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4576e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4576e-121">-WhatIf</span></span>
<span data-ttu-id="4576e-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4576e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4576e-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4576e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4576e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4576e-124">CommonParameters</span></span>
<span data-ttu-id="4576e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4576e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4576e-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4576e-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4576e-127">입력</span><span class="sxs-lookup"><span data-stu-id="4576e-127">INPUTS</span></span>

### <span data-ttu-id="4576e-128">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="4576e-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="4576e-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4576e-129">System.String</span></span>

## <span data-ttu-id="4576e-130">출력</span><span class="sxs-lookup"><span data-stu-id="4576e-130">OUTPUTS</span></span>

### <span data-ttu-id="4576e-131">AdvancedThreatProtection. ServerAdvancedThreatProtectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="4576e-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="4576e-132">상속자</span><span class="sxs-lookup"><span data-stu-id="4576e-132">NOTES</span></span>

## <span data-ttu-id="4576e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4576e-133">RELATED LINKS</span></span>
