---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343190"
---
# <span data-ttu-id="1795c-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="1795c-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="1795c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1795c-102">SYNOPSIS</span></span>
<span data-ttu-id="1795c-103">관리되는 인스턴스의 고급 데이터 보안 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1795c-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="1795c-104">구문</span><span class="sxs-lookup"><span data-stu-id="1795c-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1795c-105">설명</span><span class="sxs-lookup"><span data-stu-id="1795c-105">DESCRIPTION</span></span>
<span data-ttu-id="1795c-106">**Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet은 관리되는 인스턴스의 고급 데이터 보안 정책을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="1795c-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="1795c-107">예제</span><span class="sxs-lookup"><span data-stu-id="1795c-107">EXAMPLES</span></span>

### <span data-ttu-id="1795c-108">예제 1: 관리되는 인스턴스 고급 데이터 보안을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1795c-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="1795c-109">예제 2: 관리되는 인스턴스 리소스에서 관리되는 인스턴스 Advanced Data Security를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1795c-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="1795c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1795c-110">PARAMETERS</span></span>

### <span data-ttu-id="1795c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1795c-111">-DefaultProfile</span></span>
<span data-ttu-id="1795c-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1795c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1795c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1795c-113">-InputObject</span></span>
<span data-ttu-id="1795c-114">고급 데이터 보안 정책 작업에 사용할 관리되는 인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="1795c-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="1795c-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1795c-115">-InstanceName</span></span>
<span data-ttu-id="1795c-116">SQL 관리되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1795c-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="1795c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1795c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1795c-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1795c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="1795c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1795c-119">CommonParameters</span></span>
<span data-ttu-id="1795c-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1795c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1795c-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1795c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1795c-122">입력</span><span class="sxs-lookup"><span data-stu-id="1795c-122">INPUTS</span></span>

### <span data-ttu-id="1795c-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="1795c-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="1795c-124">System.String</span><span class="sxs-lookup"><span data-stu-id="1795c-124">System.String</span></span>

## <span data-ttu-id="1795c-125">출력</span><span class="sxs-lookup"><span data-stu-id="1795c-125">OUTPUTS</span></span>

### <span data-ttu-id="1795c-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="1795c-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="1795c-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1795c-127">NOTES</span></span>

## <span data-ttu-id="1795c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1795c-128">RELATED LINKS</span></span>
