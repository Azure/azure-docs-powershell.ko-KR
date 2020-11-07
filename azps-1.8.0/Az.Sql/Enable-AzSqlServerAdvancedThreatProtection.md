---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: aaaf417137bb1ec16150a2bf3d0ac88b64e70fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699057"
---
# <span data-ttu-id="fe0a6-101">Enable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="fe0a6-101">Enable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="fe0a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0a6-103">서버에서 고급 위협 방지를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-103">Enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="fe0a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe0a6-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe0a6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe0a6-105">DESCRIPTION</span></span>
<span data-ttu-id="fe0a6-106">AzSqlServerAdvancedThreatProtection cmdlet을 **사용** 하면 서버에서 고급 위협 방지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-106">The **Enable-AzSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="fe0a6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fe0a6-107">EXAMPLES</span></span>

### <span data-ttu-id="fe0a6-108">예제 1-서버 고급 위협 방지 사용</span><span class="sxs-lookup"><span data-stu-id="fe0a6-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="fe0a6-109">예제 2-서버 리소스에서 서버 고급 위협 방지 사용</span><span class="sxs-lookup"><span data-stu-id="fe0a6-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="fe0a6-110">변수</span><span class="sxs-lookup"><span data-stu-id="fe0a6-110">PARAMETERS</span></span>

### <span data-ttu-id="fe0a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0a6-111">-DefaultProfile</span></span>
<span data-ttu-id="fe0a6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe0a6-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe0a6-113">-InputObject</span></span>
<span data-ttu-id="fe0a6-114">고급 위협 보호 정책 작업에 사용할 서버 개체</span><span class="sxs-lookup"><span data-stu-id="fe0a6-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="fe0a6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0a6-115">-ResourceGroupName</span></span>
<span data-ttu-id="fe0a6-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe0a6-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fe0a6-117">-ServerName</span></span>
<span data-ttu-id="fe0a6-118">SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="fe0a6-119">-확인</span><span class="sxs-lookup"><span data-stu-id="fe0a6-119">-Confirm</span></span>
<span data-ttu-id="fe0a6-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe0a6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0a6-121">-WhatIf</span></span>
<span data-ttu-id="fe0a6-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe0a6-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe0a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0a6-124">CommonParameters</span></span>
<span data-ttu-id="fe0a6-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0a6-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0a6-127">입력</span><span class="sxs-lookup"><span data-stu-id="fe0a6-127">INPUTS</span></span>

### <span data-ttu-id="fe0a6-128">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="fe0a6-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="fe0a6-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fe0a6-129">System.String</span></span>

## <span data-ttu-id="fe0a6-130">출력</span><span class="sxs-lookup"><span data-stu-id="fe0a6-130">OUTPUTS</span></span>

### <span data-ttu-id="fe0a6-131">AdvancedThreatProtection. ServerAdvancedThreatProtectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="fe0a6-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="fe0a6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fe0a6-132">NOTES</span></span>

## <span data-ttu-id="fe0a6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe0a6-133">RELATED LINKS</span></span>
