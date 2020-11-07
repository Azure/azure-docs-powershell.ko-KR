---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 0812fc8aa5673f6475fb822137cffff025003d32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711634"
---
# <span data-ttu-id="8d209-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8d209-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="8d209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d209-102">SYNOPSIS</span></span>
<span data-ttu-id="8d209-103">복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d209-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d209-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d209-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d209-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8d209-105">DESCRIPTION</span></span>
<span data-ttu-id="8d209-106">**AzureRmRecoveryServicesVault** cmdlet은 현재 구독의 복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d209-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="8d209-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8d209-107">EXAMPLES</span></span>

### <span data-ttu-id="8d209-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d209-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="8d209-109">선택한 구독에서 자격 증명 모음 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="8d209-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="8d209-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="8d209-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="8d209-111">선택한 구독에서 리소스 그룹의 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d209-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="8d209-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="8d209-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="8d209-113">지정 된 이름을 사용 하 여 리소스 그룹의 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d209-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="8d209-114">변수</span><span class="sxs-lookup"><span data-stu-id="8d209-114">PARAMETERS</span></span>

### <span data-ttu-id="8d209-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8d209-115">-Name</span></span>
<span data-ttu-id="8d209-116">쿼리할 자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d209-116">Specifies the name of the vault to query for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d209-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d209-117">-ResourceGroupName</span></span>
<span data-ttu-id="8d209-118">지정 된 복구 서비스 개체를 만들거나 검색할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d209-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d209-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d209-119">-DefaultProfile</span></span>
<span data-ttu-id="8d209-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d209-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d209-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d209-121">CommonParameters</span></span>
<span data-ttu-id="8d209-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d209-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d209-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d209-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d209-124">입력</span><span class="sxs-lookup"><span data-stu-id="8d209-124">INPUTS</span></span>

### <span data-ttu-id="8d209-125">않아야</span><span class="sxs-lookup"><span data-stu-id="8d209-125">None</span></span>

## <span data-ttu-id="8d209-126">출력</span><span class="sxs-lookup"><span data-stu-id="8d209-126">OUTPUTS</span></span>

### <span data-ttu-id="8d209-127">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="8d209-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="8d209-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8d209-128">NOTES</span></span>

## <span data-ttu-id="8d209-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d209-129">RELATED LINKS</span></span>

[<span data-ttu-id="8d209-130">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8d209-130">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="8d209-131">새로운 AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8d209-131">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="8d209-132">제거-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8d209-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


