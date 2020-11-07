---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 809246520c4e6b07a1aca406ef3ec17eb9df31f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877079"
---
# <span data-ttu-id="8cfbf-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="8cfbf-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="8cfbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cfbf-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfbf-103">AD 도메인 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="8cfbf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cfbf-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cfbf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8cfbf-105">DESCRIPTION</span></span>
<span data-ttu-id="8cfbf-106">**AzVMADDomainExtension** cmdlet은 지정 된 Azure AD (Active Directory) 도메인 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="8cfbf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8cfbf-107">EXAMPLES</span></span>

### <span data-ttu-id="8cfbf-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="8cfbf-108">1:</span></span>
```

```

## <span data-ttu-id="8cfbf-109">변수</span><span class="sxs-lookup"><span data-stu-id="8cfbf-109">PARAMETERS</span></span>

### <span data-ttu-id="8cfbf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfbf-110">-DefaultProfile</span></span>
<span data-ttu-id="8cfbf-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cfbf-112">-이름</span><span class="sxs-lookup"><span data-stu-id="8cfbf-112">-Name</span></span>
<span data-ttu-id="8cfbf-113">도메인 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-113">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cfbf-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cfbf-114">-ResourceGroupName</span></span>
<span data-ttu-id="8cfbf-115">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-115">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cfbf-116">-상태</span><span class="sxs-lookup"><span data-stu-id="8cfbf-116">-Status</span></span>
<span data-ttu-id="8cfbf-117">이 cmdlet이 도메인 확장의 인스턴스 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cfbf-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="8cfbf-118">-VMName</span></span>
<span data-ttu-id="8cfbf-119">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cfbf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfbf-120">CommonParameters</span></span>
<span data-ttu-id="8cfbf-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfbf-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cfbf-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfbf-123">입력</span><span class="sxs-lookup"><span data-stu-id="8cfbf-123">INPUTS</span></span>

### <span data-ttu-id="8cfbf-124">않아야</span><span class="sxs-lookup"><span data-stu-id="8cfbf-124">None</span></span>
<span data-ttu-id="8cfbf-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8cfbf-126">출력</span><span class="sxs-lookup"><span data-stu-id="8cfbf-126">OUTPUTS</span></span>

### <span data-ttu-id="8cfbf-127">Microsoft. \*. m a m m Machineaddomainextensioncontext</span><span class="sxs-lookup"><span data-stu-id="8cfbf-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="8cfbf-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8cfbf-128">NOTES</span></span>

## <span data-ttu-id="8cfbf-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cfbf-129">RELATED LINKS</span></span>

[<span data-ttu-id="8cfbf-130">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="8cfbf-130">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


