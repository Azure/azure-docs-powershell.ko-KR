---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e4431b657c72a82f1316f5eb8b74f45fac0f04aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528252"
---
# <span data-ttu-id="3f2c0-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="3f2c0-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="3f2c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2c0-103">AD 도메인 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f2c0-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f2c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f2c0-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f2c0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3f2c0-105">DESCRIPTION</span></span>
<span data-ttu-id="3f2c0-106">**AzureRmVMADDomainExtension** cmdlet은 지정 된 Azure AD (Active Directory) 도메인 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f2c0-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="3f2c0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3f2c0-107">EXAMPLES</span></span>

## <span data-ttu-id="3f2c0-108">변수</span><span class="sxs-lookup"><span data-stu-id="3f2c0-108">PARAMETERS</span></span>

### <span data-ttu-id="3f2c0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2c0-109">-DefaultProfile</span></span>
<span data-ttu-id="3f2c0-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f2c0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f2c0-111">-이름</span><span class="sxs-lookup"><span data-stu-id="3f2c0-111">-Name</span></span>
<span data-ttu-id="3f2c0-112">도메인 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f2c0-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="3f2c0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f2c0-113">-ResourceGroupName</span></span>
<span data-ttu-id="3f2c0-114">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f2c0-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3f2c0-115">-상태</span><span class="sxs-lookup"><span data-stu-id="3f2c0-115">-Status</span></span>
<span data-ttu-id="3f2c0-116">이 cmdlet이 도메인 확장의 인스턴스 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f2c0-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="3f2c0-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="3f2c0-117">-VMName</span></span>
<span data-ttu-id="3f2c0-118">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f2c0-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="3f2c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2c0-119">CommonParameters</span></span>
<span data-ttu-id="3f2c0-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f2c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2c0-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f2c0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2c0-122">입력</span><span class="sxs-lookup"><span data-stu-id="3f2c0-122">INPUTS</span></span>

## <span data-ttu-id="3f2c0-123">출력</span><span class="sxs-lookup"><span data-stu-id="3f2c0-123">OUTPUTS</span></span>

## <span data-ttu-id="3f2c0-124">상속자</span><span class="sxs-lookup"><span data-stu-id="3f2c0-124">NOTES</span></span>

## <span data-ttu-id="3f2c0-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f2c0-125">RELATED LINKS</span></span>

[<span data-ttu-id="3f2c0-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="3f2c0-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


