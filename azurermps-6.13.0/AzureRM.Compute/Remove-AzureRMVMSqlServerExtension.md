---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 83f697733d56ae7d99bc0b2660b5abbaca15a71f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536723"
---
# <span data-ttu-id="3b6fa-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3b6fa-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="3b6fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3b6fa-103">가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6fa-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b6fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b6fa-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b6fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3b6fa-105">DESCRIPTION</span></span>
<span data-ttu-id="3b6fa-106">**AzureRmVMSqlServerExtension** cmdlet은 가상 머신에서 AzureSQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6fa-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="3b6fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3b6fa-107">EXAMPLES</span></span>

### <span data-ttu-id="3b6fa-108">예제 1: SQL Server 확장 제거</span><span class="sxs-lookup"><span data-stu-id="3b6fa-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="3b6fa-109">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6fa-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="3b6fa-110">변수</span><span class="sxs-lookup"><span data-stu-id="3b6fa-110">PARAMETERS</span></span>

### <span data-ttu-id="3b6fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b6fa-111">-DefaultProfile</span></span>
<span data-ttu-id="3b6fa-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b6fa-113">-이름</span><span class="sxs-lookup"><span data-stu-id="3b6fa-113">-Name</span></span>
<span data-ttu-id="3b6fa-114">이 cmdlet이 제거 하는 확장 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6fa-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3b6fa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b6fa-115">-ResourceGroupName</span></span>
<span data-ttu-id="3b6fa-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6fa-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3b6fa-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="3b6fa-117">-VMName</span></span>
<span data-ttu-id="3b6fa-118">이 cmdlet에서 SQL Server 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6fa-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="3b6fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b6fa-119">CommonParameters</span></span>
<span data-ttu-id="3b6fa-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b6fa-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b6fa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b6fa-122">입력</span><span class="sxs-lookup"><span data-stu-id="3b6fa-122">INPUTS</span></span>

### <span data-ttu-id="3b6fa-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3b6fa-123">System.String</span></span>

## <span data-ttu-id="3b6fa-124">출력</span><span class="sxs-lookup"><span data-stu-id="3b6fa-124">OUTPUTS</span></span>

### <span data-ttu-id="3b6fa-125">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6fa-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3b6fa-126">상속자</span><span class="sxs-lookup"><span data-stu-id="3b6fa-126">NOTES</span></span>

## <span data-ttu-id="3b6fa-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b6fa-127">RELATED LINKS</span></span>

[<span data-ttu-id="3b6fa-128">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3b6fa-128">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="3b6fa-129">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3b6fa-129">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


