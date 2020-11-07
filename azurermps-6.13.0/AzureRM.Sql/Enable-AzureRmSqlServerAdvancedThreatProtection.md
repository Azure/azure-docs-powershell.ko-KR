---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/enable-azurermsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Enable-AzureRmSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Enable-AzureRmSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: 1276ba100a795ca113f1f09064bc46dfdfddf39b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704113"
---
# <span data-ttu-id="f3ea3-101">Enable-AzureRmSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f3ea3-101">Enable-AzureRmSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="f3ea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ea3-103">서버에서 고급 위협 방지를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ea3-103">Enables Advanced Threat Protection on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3ea3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3ea3-104">SYNTAX</span></span>

```
Enable-AzureRmSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ea3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f3ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ea3-106">AzureRmSqlServerAdvancedThreatProtection cmdlet을 **사용** 하면 서버에서 고급 위협 방지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ea3-106">The **Enable-AzureRmSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="f3ea3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f3ea3-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ea3-108">예제 1-서버 고급 위협 방지 사용</span><span class="sxs-lookup"><span data-stu-id="f3ea3-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzureRmSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="f3ea3-109">예제 2-서버 리소스에서 서버 고급 위협 방지 사용</span><span class="sxs-lookup"><span data-stu-id="f3ea3-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzureRmSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="f3ea3-110">변수</span><span class="sxs-lookup"><span data-stu-id="f3ea3-110">PARAMETERS</span></span>

### <span data-ttu-id="f3ea3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ea3-111">-DefaultProfile</span></span>
<span data-ttu-id="f3ea3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ea3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ea3-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3ea3-113">-InputObject</span></span>
<span data-ttu-id="f3ea3-114">고급 위협 보호 정책 작업에 사용할 서버 개체</span><span class="sxs-lookup"><span data-stu-id="f3ea3-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="f3ea3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ea3-115">-ResourceGroupName</span></span>
<span data-ttu-id="f3ea3-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ea3-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3ea3-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3ea3-117">-ServerName</span></span>
<span data-ttu-id="f3ea3-118">SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ea3-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="f3ea3-119">-확인</span><span class="sxs-lookup"><span data-stu-id="f3ea3-119">-Confirm</span></span>
<span data-ttu-id="f3ea3-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ea3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ea3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ea3-121">-WhatIf</span></span>
<span data-ttu-id="f3ea3-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3ea3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3ea3-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ea3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ea3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ea3-124">CommonParameters</span></span>
<span data-ttu-id="f3ea3-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ea3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ea3-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ea3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ea3-127">입력</span><span class="sxs-lookup"><span data-stu-id="f3ea3-127">INPUTS</span></span>

### <span data-ttu-id="f3ea3-128">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="f3ea3-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="f3ea3-129">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3ea3-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f3ea3-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3ea3-130">System.String</span></span>

## <span data-ttu-id="f3ea3-131">출력</span><span class="sxs-lookup"><span data-stu-id="f3ea3-131">OUTPUTS</span></span>

### <span data-ttu-id="f3ea3-132">AdvancedThreatProtection. ServerAdvancedThreatProtectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="f3ea3-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="f3ea3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f3ea3-133">NOTES</span></span>

## <span data-ttu-id="f3ea3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3ea3-134">RELATED LINKS</span></span>
