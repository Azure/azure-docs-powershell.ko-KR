---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: 4dd2042ae3c7e84b9a7a82dde19fb5848229f51c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967264"
---
# <span data-ttu-id="d4bc8-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="d4bc8-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="d4bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="d4bc8-103">SQL 가상 머신 구성에서 SQL 가상 머신 그룹을 상대로 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="d4bc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="d4bc8-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4bc8-105">설명</span><span class="sxs-lookup"><span data-stu-id="d4bc8-105">DESCRIPTION</span></span>
<span data-ttu-id="d4bc8-106">Set-AzSqlVMConfigGroup cmdlet은 SQL 가상 머신 구성에 대한 sql Virtual Machine 그룹에 조인하는 데 필요한 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="d4bc8-107">예제</span><span class="sxs-lookup"><span data-stu-id="d4bc8-107">EXAMPLES</span></span>

### <span data-ttu-id="d4bc8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d4bc8-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="d4bc8-109">SQL 가상 머신 구성의 그룹 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="d4bc8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d4bc8-110">PARAMETERS</span></span>

### <span data-ttu-id="d4bc8-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="d4bc8-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="d4bc8-112">클러스터 부트스트레이프 계정에 대한 암호</span><span class="sxs-lookup"><span data-stu-id="d4bc8-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4bc8-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="d4bc8-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="d4bc8-114">클러스터 운영자 계정에 대한 암호</span><span class="sxs-lookup"><span data-stu-id="d4bc8-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4bc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4bc8-115">-DefaultProfile</span></span>
<span data-ttu-id="d4bc8-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4bc8-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="d4bc8-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="d4bc8-118">서비스 계정의 SQL 암호</span><span class="sxs-lookup"><span data-stu-id="d4bc8-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4bc8-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="d4bc8-119">-SqlVM</span></span>
<span data-ttu-id="d4bc8-120">그룹 SQL 추가할 가상 머신 구성</span><span class="sxs-lookup"><span data-stu-id="d4bc8-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4bc8-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="d4bc8-121">-SqlVMGroup</span></span>
<span data-ttu-id="d4bc8-122">가상 머신의 SQL 그룹</span><span class="sxs-lookup"><span data-stu-id="d4bc8-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4bc8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4bc8-123">CommonParameters</span></span>
<span data-ttu-id="d4bc8-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4bc8-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4bc8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4bc8-126">입력</span><span class="sxs-lookup"><span data-stu-id="d4bc8-126">INPUTS</span></span>

### <span data-ttu-id="d4bc8-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d4bc8-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d4bc8-128">출력</span><span class="sxs-lookup"><span data-stu-id="d4bc8-128">OUTPUTS</span></span>

### <span data-ttu-id="d4bc8-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d4bc8-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d4bc8-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d4bc8-130">NOTES</span></span>

## <span data-ttu-id="d4bc8-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4bc8-131">RELATED LINKS</span></span>
