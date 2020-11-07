---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: a2615f5d016d16edb1201e88c31a8be62771ae59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874002"
---
# <span data-ttu-id="851c3-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="851c3-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="851c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="851c3-102">SYNOPSIS</span></span>
<span data-ttu-id="851c3-103">Sql 가상 컴퓨터 구성에서 sql 가상 컴퓨터 그룹과 관련 된 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="851c3-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="851c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="851c3-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="851c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="851c3-105">DESCRIPTION</span></span>
<span data-ttu-id="851c3-106">Set-AzSqlVMConfigGroup cmdlet은 sql 가상 컴퓨터 구성에 대 한 sql 가상 컴퓨터 그룹에 참가 하기 위해 필요한 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="851c3-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="851c3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="851c3-107">EXAMPLES</span></span>

### <span data-ttu-id="851c3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="851c3-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="851c3-109">Sql 가상 컴퓨터 구성의 그룹 informations를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="851c3-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="851c3-110">변수</span><span class="sxs-lookup"><span data-stu-id="851c3-110">PARAMETERS</span></span>

### <span data-ttu-id="851c3-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="851c3-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="851c3-112">클러스터 부트스트랩 계정에 대 한 암호</span><span class="sxs-lookup"><span data-stu-id="851c3-112">Password for the cluster bootstrap account</span></span>

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

### <span data-ttu-id="851c3-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="851c3-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="851c3-114">클러스터 운영자 계정에 대 한 암호</span><span class="sxs-lookup"><span data-stu-id="851c3-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="851c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851c3-115">-DefaultProfile</span></span>
<span data-ttu-id="851c3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="851c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="851c3-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="851c3-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="851c3-118">SQL 서비스 계정에 대 한 암호</span><span class="sxs-lookup"><span data-stu-id="851c3-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="851c3-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="851c3-119">-SqlVM</span></span>
<span data-ttu-id="851c3-120">그룹 구성원 자격이 추가 되는 SQL 가상 컴퓨터 구성</span><span class="sxs-lookup"><span data-stu-id="851c3-120">The SQL virtual machine configuration which group membership will be added to</span></span>

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

### <span data-ttu-id="851c3-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="851c3-121">-SqlVMGroup</span></span>
<span data-ttu-id="851c3-122">SQL 가상 컴퓨터를 포함 하는 그룹</span><span class="sxs-lookup"><span data-stu-id="851c3-122">The group the SQL virtual machine will be part of</span></span>

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

### <span data-ttu-id="851c3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851c3-123">CommonParameters</span></span>
<span data-ttu-id="851c3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="851c3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851c3-125">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="851c3-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851c3-126">입력</span><span class="sxs-lookup"><span data-stu-id="851c3-126">INPUTS</span></span>

### <span data-ttu-id="851c3-127">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="851c3-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="851c3-128">출력</span><span class="sxs-lookup"><span data-stu-id="851c3-128">OUTPUTS</span></span>

### <span data-ttu-id="851c3-129">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="851c3-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="851c3-130">상속자</span><span class="sxs-lookup"><span data-stu-id="851c3-130">NOTES</span></span>

## <span data-ttu-id="851c3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="851c3-131">RELATED LINKS</span></span>
