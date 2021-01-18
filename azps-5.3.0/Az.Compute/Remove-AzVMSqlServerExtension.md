---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495968"
---
# <span data-ttu-id="0bf1c-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0bf1c-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="0bf1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bf1c-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf1c-103">가상 머신에서 SQL Server 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="0bf1c-104">구문</span><span class="sxs-lookup"><span data-stu-id="0bf1c-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bf1c-105">설명</span><span class="sxs-lookup"><span data-stu-id="0bf1c-105">DESCRIPTION</span></span>
<span data-ttu-id="0bf1c-106">**Remove-AzVMSqlServerExtension** cmdlet은 가상 머신에서 AzureSQL 서버 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="0bf1c-107">예제</span><span class="sxs-lookup"><span data-stu-id="0bf1c-107">EXAMPLES</span></span>

### <span data-ttu-id="0bf1c-108">예제 1: 확장 SQL Server 제거</span><span class="sxs-lookup"><span data-stu-id="0bf1c-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="0bf1c-109">이 명령은 ContosoVM22라는 SQL Server 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="0bf1c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bf1c-110">PARAMETERS</span></span>

### <span data-ttu-id="0bf1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf1c-111">-DefaultProfile</span></span>
<span data-ttu-id="0bf1c-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bf1c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0bf1c-113">-Name</span></span>
<span data-ttu-id="0bf1c-114">이 cmdlet이 SQL Server 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bf1c-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0bf1c-115">-NoWait</span></span>
<span data-ttu-id="0bf1c-116">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0bf1c-117">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0bf1c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bf1c-118">-ResourceGroupName</span></span>
<span data-ttu-id="0bf1c-119">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0bf1c-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="0bf1c-120">-VMName</span></span>
<span data-ttu-id="0bf1c-121">이 cmdlet이 확장을 제거한 가상 머신의 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bf1c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf1c-122">CommonParameters</span></span>
<span data-ttu-id="0bf1c-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf1c-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf1c-125">입력</span><span class="sxs-lookup"><span data-stu-id="0bf1c-125">INPUTS</span></span>

### <span data-ttu-id="0bf1c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0bf1c-126">System.String</span></span>

## <span data-ttu-id="0bf1c-127">출력</span><span class="sxs-lookup"><span data-stu-id="0bf1c-127">OUTPUTS</span></span>

### <span data-ttu-id="0bf1c-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0bf1c-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0bf1c-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0bf1c-129">NOTES</span></span>

## <span data-ttu-id="0bf1c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bf1c-130">RELATED LINKS</span></span>

[<span data-ttu-id="0bf1c-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0bf1c-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="0bf1c-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0bf1c-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


