---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bd9b47b54cb609a06da10488007f55d91d157b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533888"
---
# <span data-ttu-id="5a05a-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5a05a-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="5a05a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a05a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a05a-103">복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a05a-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a05a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a05a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a05a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5a05a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a05a-106">**AzureRmRecoveryServicesVault** cmdlet은 현재 구독의 복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a05a-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="5a05a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5a05a-107">EXAMPLES</span></span>

## <span data-ttu-id="5a05a-108">변수</span><span class="sxs-lookup"><span data-stu-id="5a05a-108">PARAMETERS</span></span>

### <span data-ttu-id="5a05a-109">-이름</span><span class="sxs-lookup"><span data-stu-id="5a05a-109">-Name</span></span>
<span data-ttu-id="5a05a-110">쿼리할 자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a05a-110">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a05a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a05a-111">-ResourceGroupName</span></span>
<span data-ttu-id="5a05a-112">지정 된 복구 서비스 개체를 만들거나 검색할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a05a-112">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a05a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a05a-113">-DefaultProfile</span></span>
<span data-ttu-id="5a05a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a05a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a05a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a05a-115">CommonParameters</span></span>
<span data-ttu-id="5a05a-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a05a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a05a-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a05a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a05a-118">입력</span><span class="sxs-lookup"><span data-stu-id="5a05a-118">INPUTS</span></span>

## <span data-ttu-id="5a05a-119">출력</span><span class="sxs-lookup"><span data-stu-id="5a05a-119">OUTPUTS</span></span>

### <span data-ttu-id="5a05a-120">ARSVault의 목록 ' 1 [Microsoft. t e;]</span><span class="sxs-lookup"><span data-stu-id="5a05a-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="5a05a-121">상속자</span><span class="sxs-lookup"><span data-stu-id="5a05a-121">NOTES</span></span>

## <span data-ttu-id="5a05a-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a05a-122">RELATED LINKS</span></span>

[<span data-ttu-id="5a05a-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="5a05a-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="5a05a-124">새로운 AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5a05a-124">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="5a05a-125">제거-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5a05a-125">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


