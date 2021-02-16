---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176692"
---
# <span data-ttu-id="29fd1-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="29fd1-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="29fd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="29fd1-103">SQL 가상 머신 구성에서 SQL 가상 머신 그룹을 상대로 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="29fd1-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="29fd1-104">구문</span><span class="sxs-lookup"><span data-stu-id="29fd1-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29fd1-105">설명</span><span class="sxs-lookup"><span data-stu-id="29fd1-105">DESCRIPTION</span></span>
<span data-ttu-id="29fd1-106">Set-AzSqlVMConfigGroup cmdlet은 SQL 가상 머신 구성에 대한 SQL 가상 머신 그룹을 조인하는 데 필요한 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="29fd1-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="29fd1-107">예제</span><span class="sxs-lookup"><span data-stu-id="29fd1-107">EXAMPLES</span></span>

### <span data-ttu-id="29fd1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="29fd1-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="29fd1-109">SQL 가상 머신 구성의 그룹 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="29fd1-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="29fd1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29fd1-110">PARAMETERS</span></span>

### <span data-ttu-id="29fd1-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="29fd1-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="29fd1-112">클러스터 부트스트힙 계정에 대한 암호</span><span class="sxs-lookup"><span data-stu-id="29fd1-112">Password for the cluster bootstrap account</span></span>

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

### <span data-ttu-id="29fd1-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="29fd1-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="29fd1-114">클러스터 운영자 계정에 대한 암호</span><span class="sxs-lookup"><span data-stu-id="29fd1-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="29fd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29fd1-115">-DefaultProfile</span></span>
<span data-ttu-id="29fd1-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29fd1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29fd1-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="29fd1-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="29fd1-118">SQL 서비스 계정에 대한 암호</span><span class="sxs-lookup"><span data-stu-id="29fd1-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="29fd1-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="29fd1-119">-SqlVM</span></span>
<span data-ttu-id="29fd1-120">그룹 SQL 추가할 가상 머신 구성</span><span class="sxs-lookup"><span data-stu-id="29fd1-120">The SQL virtual machine configuration which group membership will be added to</span></span>

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

### <span data-ttu-id="29fd1-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="29fd1-121">-SqlVMGroup</span></span>
<span data-ttu-id="29fd1-122">가상 머신이 SQL 그룹</span><span class="sxs-lookup"><span data-stu-id="29fd1-122">The group the SQL virtual machine will be part of</span></span>

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

### <span data-ttu-id="29fd1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29fd1-123">CommonParameters</span></span>
<span data-ttu-id="29fd1-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29fd1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29fd1-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29fd1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29fd1-126">입력</span><span class="sxs-lookup"><span data-stu-id="29fd1-126">INPUTS</span></span>

### <span data-ttu-id="29fd1-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="29fd1-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="29fd1-128">출력</span><span class="sxs-lookup"><span data-stu-id="29fd1-128">OUTPUTS</span></span>

### <span data-ttu-id="29fd1-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="29fd1-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="29fd1-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29fd1-130">NOTES</span></span>

## <span data-ttu-id="29fd1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29fd1-131">RELATED LINKS</span></span>
