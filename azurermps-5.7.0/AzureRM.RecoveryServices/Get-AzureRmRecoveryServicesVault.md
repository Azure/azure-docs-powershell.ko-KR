---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bbc059751ee4713b59f6b915efe32bdf57419be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533684"
---
# <span data-ttu-id="dadf1-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="dadf1-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="dadf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dadf1-102">SYNOPSIS</span></span>
<span data-ttu-id="dadf1-103">복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dadf1-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dadf1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dadf1-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dadf1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dadf1-105">DESCRIPTION</span></span>
<span data-ttu-id="dadf1-106">**AzureRmRecoveryServicesVault** cmdlet은 현재 구독의 복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dadf1-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="dadf1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dadf1-107">EXAMPLES</span></span>

### <span data-ttu-id="dadf1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dadf1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="dadf1-109">선택한 구독에서 자격 증명 모음 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="dadf1-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="dadf1-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="dadf1-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="dadf1-111">선택한 구독에서 리소스 그룹의 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dadf1-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="dadf1-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="dadf1-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="dadf1-113">지정 된 이름을 사용 하 여 리소스 그룹의 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dadf1-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="dadf1-114">변수</span><span class="sxs-lookup"><span data-stu-id="dadf1-114">PARAMETERS</span></span>

### <span data-ttu-id="dadf1-115">-이름</span><span class="sxs-lookup"><span data-stu-id="dadf1-115">-Name</span></span>
<span data-ttu-id="dadf1-116">쿼리할 자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dadf1-116">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="dadf1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dadf1-117">-ResourceGroupName</span></span>
<span data-ttu-id="dadf1-118">지정 된 복구 서비스 개체를 만들거나 검색할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dadf1-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="dadf1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dadf1-119">-DefaultProfile</span></span>
<span data-ttu-id="dadf1-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dadf1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dadf1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dadf1-121">CommonParameters</span></span>
<span data-ttu-id="dadf1-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dadf1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dadf1-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dadf1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dadf1-124">입력</span><span class="sxs-lookup"><span data-stu-id="dadf1-124">INPUTS</span></span>

### <span data-ttu-id="dadf1-125">않아야</span><span class="sxs-lookup"><span data-stu-id="dadf1-125">None</span></span>
<span data-ttu-id="dadf1-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dadf1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dadf1-127">출력</span><span class="sxs-lookup"><span data-stu-id="dadf1-127">OUTPUTS</span></span>

### <span data-ttu-id="dadf1-128">ARSVault의 목록 ' 1 [Microsoft. t e;]</span><span class="sxs-lookup"><span data-stu-id="dadf1-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="dadf1-129">상속자</span><span class="sxs-lookup"><span data-stu-id="dadf1-129">NOTES</span></span>

## <span data-ttu-id="dadf1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dadf1-130">RELATED LINKS</span></span>

[<span data-ttu-id="dadf1-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="dadf1-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="dadf1-132">새로운 AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="dadf1-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="dadf1-133">제거-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="dadf1-133">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


