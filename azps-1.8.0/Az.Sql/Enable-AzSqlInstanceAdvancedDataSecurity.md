---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: faf93387f068c6ee8e83653d31b96a1f3ecdef70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699058"
---
# <span data-ttu-id="be499-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="be499-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="be499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be499-102">SYNOPSIS</span></span>
<span data-ttu-id="be499-103">관리 되는 인스턴스에서 고급 데이터 보안을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be499-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="be499-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be499-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be499-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be499-105">DESCRIPTION</span></span>
<span data-ttu-id="be499-106">AzSqlInstanceAdvancedDataSecurity cmdlet을 **사용** 하면 관리 되는 인스턴스에서 고급 데이터 보안을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be499-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="be499-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be499-107">EXAMPLES</span></span>

### <span data-ttu-id="be499-108">예제 1-관리 되는 인스턴스 사용 고급 데이터 보안</span><span class="sxs-lookup"><span data-stu-id="be499-108">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="be499-109">예제 2-서버 리소스의 관리 되는 인스턴스 고급 데이터 보안 사용</span><span class="sxs-lookup"><span data-stu-id="be499-109">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="be499-110">변수</span><span class="sxs-lookup"><span data-stu-id="be499-110">PARAMETERS</span></span>

### <span data-ttu-id="be499-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be499-111">-DefaultProfile</span></span>
<span data-ttu-id="be499-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be499-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be499-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be499-113">-InputObject</span></span>
<span data-ttu-id="be499-114">고급 데이터 보안 정책 작업에 사용할 관리 되는 인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="be499-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be499-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="be499-115">-InstanceName</span></span>
<span data-ttu-id="be499-116">SQL Database 관리 되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be499-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="be499-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be499-117">-ResourceGroupName</span></span>
<span data-ttu-id="be499-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be499-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="be499-119">-확인</span><span class="sxs-lookup"><span data-stu-id="be499-119">-Confirm</span></span>
<span data-ttu-id="be499-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be499-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be499-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be499-121">-WhatIf</span></span>
<span data-ttu-id="be499-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be499-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be499-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be499-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be499-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be499-124">CommonParameters</span></span>
<span data-ttu-id="be499-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be499-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be499-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be499-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be499-127">입력</span><span class="sxs-lookup"><span data-stu-id="be499-127">INPUTS</span></span>

### <span data-ttu-id="be499-128">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="be499-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="be499-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be499-129">System.String</span></span>

## <span data-ttu-id="be499-130">출력</span><span class="sxs-lookup"><span data-stu-id="be499-130">OUTPUTS</span></span>

### <span data-ttu-id="be499-131">AdvancedThreatProtection. ManagedInstanceAdvancedDataSecurityPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="be499-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="be499-132">상속자</span><span class="sxs-lookup"><span data-stu-id="be499-132">NOTES</span></span>

## <span data-ttu-id="be499-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be499-133">RELATED LINKS</span></span>
