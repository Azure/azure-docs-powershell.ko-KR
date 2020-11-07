---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 630df5bbe6677c7019d372a2a6977cc4c724a421
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701274"
---
# <span data-ttu-id="9225f-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9225f-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="9225f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9225f-102">SYNOPSIS</span></span>
<span data-ttu-id="9225f-103">가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9225f-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="9225f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9225f-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9225f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9225f-105">DESCRIPTION</span></span>
<span data-ttu-id="9225f-106">**AzVMSqlServerExtension** cmdlet은 가상 머신에서 AzureSQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9225f-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="9225f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9225f-107">EXAMPLES</span></span>

### <span data-ttu-id="9225f-108">예제 1: SQL Server 확장 제거</span><span class="sxs-lookup"><span data-stu-id="9225f-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="9225f-109">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9225f-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="9225f-110">변수</span><span class="sxs-lookup"><span data-stu-id="9225f-110">PARAMETERS</span></span>

### <span data-ttu-id="9225f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9225f-111">-DefaultProfile</span></span>
<span data-ttu-id="9225f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9225f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9225f-113">-이름</span><span class="sxs-lookup"><span data-stu-id="9225f-113">-Name</span></span>
<span data-ttu-id="9225f-114">이 cmdlet이 제거 하는 확장 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9225f-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9225f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9225f-115">-ResourceGroupName</span></span>
<span data-ttu-id="9225f-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9225f-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9225f-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="9225f-117">-VMName</span></span>
<span data-ttu-id="9225f-118">이 cmdlet에서 SQL Server 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9225f-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="9225f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9225f-119">CommonParameters</span></span>
<span data-ttu-id="9225f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9225f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9225f-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9225f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9225f-122">입력</span><span class="sxs-lookup"><span data-stu-id="9225f-122">INPUTS</span></span>

### <span data-ttu-id="9225f-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9225f-123">System.String</span></span>

## <span data-ttu-id="9225f-124">출력</span><span class="sxs-lookup"><span data-stu-id="9225f-124">OUTPUTS</span></span>

### <span data-ttu-id="9225f-125">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="9225f-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9225f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="9225f-126">NOTES</span></span>

## <span data-ttu-id="9225f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9225f-127">RELATED LINKS</span></span>

[<span data-ttu-id="9225f-128">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9225f-128">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="9225f-129">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9225f-129">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


