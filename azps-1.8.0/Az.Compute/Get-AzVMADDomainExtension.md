---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 2ec4ec1898e79fd7f7f35a406f2a99f9dd2da6fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701353"
---
# <span data-ttu-id="c7aff-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c7aff-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="c7aff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7aff-102">SYNOPSIS</span></span>
<span data-ttu-id="c7aff-103">AD 도메인 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7aff-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="c7aff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7aff-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7aff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c7aff-105">DESCRIPTION</span></span>
<span data-ttu-id="c7aff-106">**AzVMADDomainExtension** cmdlet은 지정 된 Azure AD (Active Directory) 도메인 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7aff-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="c7aff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c7aff-107">EXAMPLES</span></span>

## <span data-ttu-id="c7aff-108">변수</span><span class="sxs-lookup"><span data-stu-id="c7aff-108">PARAMETERS</span></span>

### <span data-ttu-id="c7aff-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7aff-109">-DefaultProfile</span></span>
<span data-ttu-id="c7aff-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aff-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7aff-111">-이름</span><span class="sxs-lookup"><span data-stu-id="c7aff-111">-Name</span></span>
<span data-ttu-id="c7aff-112">도메인 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aff-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="c7aff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7aff-113">-ResourceGroupName</span></span>
<span data-ttu-id="c7aff-114">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aff-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c7aff-115">-상태</span><span class="sxs-lookup"><span data-stu-id="c7aff-115">-Status</span></span>
<span data-ttu-id="c7aff-116">이 cmdlet이 도메인 확장의 인스턴스 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7aff-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7aff-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="c7aff-117">-VMName</span></span>
<span data-ttu-id="c7aff-118">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aff-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="c7aff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7aff-119">CommonParameters</span></span>
<span data-ttu-id="c7aff-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7aff-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7aff-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7aff-122">입력</span><span class="sxs-lookup"><span data-stu-id="c7aff-122">INPUTS</span></span>

### <span data-ttu-id="c7aff-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7aff-123">System.String</span></span>

### <span data-ttu-id="c7aff-124">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c7aff-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7aff-125">출력</span><span class="sxs-lookup"><span data-stu-id="c7aff-125">OUTPUTS</span></span>

### <span data-ttu-id="c7aff-126">Microsoft. \*. m a m m Machineaddomainextensioncontext</span><span class="sxs-lookup"><span data-stu-id="c7aff-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="c7aff-127">상속자</span><span class="sxs-lookup"><span data-stu-id="c7aff-127">NOTES</span></span>

## <span data-ttu-id="c7aff-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7aff-128">RELATED LINKS</span></span>

[<span data-ttu-id="c7aff-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c7aff-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


