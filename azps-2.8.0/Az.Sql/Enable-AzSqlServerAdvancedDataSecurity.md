---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: c2c3b634eb5a9e031c375a6cc696298becd58e8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873536"
---
# <span data-ttu-id="9606c-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="9606c-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="9606c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9606c-102">SYNOPSIS</span></span>
<span data-ttu-id="9606c-103">서버에서 고급 데이터 보안을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="9606c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9606c-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9606c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9606c-105">DESCRIPTION</span></span>
<span data-ttu-id="9606c-106">AzSqlServerAdvancedDataSecurity cmdlet을 **사용** 하면 서버에서 고급 데이터 보안을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="9606c-107">고급 데이터 보안은 서버에 대 한 데이터 분류, 취약점 평가 및 고급 위협 보호를 포함 하는 통합 된 보안 패키지입니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="9606c-108">취약점 평가를 저장 하기 위해 새로운 저장소 계정이 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="9606c-109">이전에이 용도로 만든 저장소 계정이 아닌 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="9606c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9606c-110">EXAMPLES</span></span>

### <span data-ttu-id="9606c-111">예제 1-서버 고급 데이터 보안 사용</span><span class="sxs-lookup"><span data-stu-id="9606c-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="9606c-112">예제 2-서버 리소스에서 서버 고급 데이터 보안 설정</span><span class="sxs-lookup"><span data-stu-id="9606c-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="9606c-113">변수</span><span class="sxs-lookup"><span data-stu-id="9606c-113">PARAMETERS</span></span>

### <span data-ttu-id="9606c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9606c-114">-AsJob</span></span>
<span data-ttu-id="9606c-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9606c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9606c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9606c-116">-DefaultProfile</span></span>
<span data-ttu-id="9606c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9606c-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9606c-118">-DeploymentName</span></span>
<span data-ttu-id="9606c-119">고급 데이터 보안 배포에 대 한 사용자 지정 이름 제공</span><span class="sxs-lookup"><span data-stu-id="9606c-119">Supply a custom name for Advanced Data Security deployment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9606c-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="9606c-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="9606c-121">취약점 평가를 자동으로 사용 하지 않음 (이는 저장소 계정을 만들지 않음)</span><span class="sxs-lookup"><span data-stu-id="9606c-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="9606c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9606c-122">-InputObject</span></span>
<span data-ttu-id="9606c-123">고급 데이터 보안 정책 작업에 사용할 서버 개체</span><span class="sxs-lookup"><span data-stu-id="9606c-123">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="9606c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9606c-124">-ResourceGroupName</span></span>
<span data-ttu-id="9606c-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="9606c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9606c-126">-ServerName</span></span>
<span data-ttu-id="9606c-127">SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-127">SQL Database server name.</span></span>

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

### <span data-ttu-id="9606c-128">-확인</span><span class="sxs-lookup"><span data-stu-id="9606c-128">-Confirm</span></span>
<span data-ttu-id="9606c-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9606c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9606c-130">-WhatIf</span></span>
<span data-ttu-id="9606c-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9606c-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9606c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9606c-133">CommonParameters</span></span>
<span data-ttu-id="9606c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9606c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9606c-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9606c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9606c-136">입력</span><span class="sxs-lookup"><span data-stu-id="9606c-136">INPUTS</span></span>

### <span data-ttu-id="9606c-137">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="9606c-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="9606c-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9606c-138">System.String</span></span>

## <span data-ttu-id="9606c-139">출력</span><span class="sxs-lookup"><span data-stu-id="9606c-139">OUTPUTS</span></span>

### <span data-ttu-id="9606c-140">AdvancedThreatProtection. ServerAdvancedDataSecurityPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="9606c-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="9606c-141">상속자</span><span class="sxs-lookup"><span data-stu-id="9606c-141">NOTES</span></span>

## <span data-ttu-id="9606c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9606c-142">RELATED LINKS</span></span>
