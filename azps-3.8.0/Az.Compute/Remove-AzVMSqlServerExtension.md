---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043661"
---
# <span data-ttu-id="2a4b8-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2a4b8-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="2a4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4b8-103">가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="2a4b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a4b8-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a4b8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2a4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="2a4b8-106">**AzVMSqlServerExtension** cmdlet은 가상 머신에서 AzureSQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="2a4b8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2a4b8-107">EXAMPLES</span></span>

### <span data-ttu-id="2a4b8-108">예제 1: SQL Server 확장 제거</span><span class="sxs-lookup"><span data-stu-id="2a4b8-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="2a4b8-109">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="2a4b8-110">변수</span><span class="sxs-lookup"><span data-stu-id="2a4b8-110">PARAMETERS</span></span>

### <span data-ttu-id="2a4b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4b8-111">-DefaultProfile</span></span>
<span data-ttu-id="2a4b8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a4b8-113">-이름</span><span class="sxs-lookup"><span data-stu-id="2a4b8-113">-Name</span></span>
<span data-ttu-id="2a4b8-114">이 cmdlet이 제거 하는 확장 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2a4b8-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2a4b8-115">-NoWait</span></span>
<span data-ttu-id="2a4b8-116">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2a4b8-117">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2a4b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a4b8-118">-ResourceGroupName</span></span>
<span data-ttu-id="2a4b8-119">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2a4b8-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="2a4b8-120">-VMName</span></span>
<span data-ttu-id="2a4b8-121">이 cmdlet에서 SQL Server 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="2a4b8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4b8-122">CommonParameters</span></span>
<span data-ttu-id="2a4b8-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4b8-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4b8-125">입력</span><span class="sxs-lookup"><span data-stu-id="2a4b8-125">INPUTS</span></span>

### <span data-ttu-id="2a4b8-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2a4b8-126">System.String</span></span>

## <span data-ttu-id="2a4b8-127">출력</span><span class="sxs-lookup"><span data-stu-id="2a4b8-127">OUTPUTS</span></span>

### <span data-ttu-id="2a4b8-128">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="2a4b8-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2a4b8-129">상속자</span><span class="sxs-lookup"><span data-stu-id="2a4b8-129">NOTES</span></span>

## <span data-ttu-id="2a4b8-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a4b8-130">RELATED LINKS</span></span>

[<span data-ttu-id="2a4b8-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2a4b8-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="2a4b8-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2a4b8-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


