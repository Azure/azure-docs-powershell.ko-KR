---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 3607835496aa6f99cfd2b42383654180d6b12331
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872646"
---
# <span data-ttu-id="ecb26-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ecb26-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="ecb26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb26-102">SYNOPSIS</span></span>

<span data-ttu-id="ecb26-103">복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ecb26-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="ecb26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecb26-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecb26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ecb26-105">DESCRIPTION</span></span>

<span data-ttu-id="ecb26-106">**AzRecoveryServicesVault** cmdlet은 현재 구독의 복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ecb26-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="ecb26-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ecb26-107">EXAMPLES</span></span>

### <span data-ttu-id="ecb26-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ecb26-108">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="ecb26-109">선택한 구독에서 자격 증명 모음 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="ecb26-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="ecb26-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="ecb26-110">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="ecb26-111">선택한 구독에서 리소스 그룹의 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ecb26-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="ecb26-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="ecb26-112">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="ecb26-113">지정 된 이름을 사용 하 여 리소스 그룹의 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ecb26-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="ecb26-114">변수</span><span class="sxs-lookup"><span data-stu-id="ecb26-114">PARAMETERS</span></span>

### <span data-ttu-id="ecb26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb26-115">-DefaultProfile</span></span>

<span data-ttu-id="ecb26-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb26-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecb26-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ecb26-117">-Name</span></span>

<span data-ttu-id="ecb26-118">쿼리할 자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb26-118">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="ecb26-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb26-119">-ResourceGroupName</span></span>

<span data-ttu-id="ecb26-120">지정 된 복구 서비스 개체를 검색할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb26-120">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="ecb26-121">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb26-121">-CommonParameters</span></span>

<span data-ttu-id="ecb26-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb26-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb26-123">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ecb26-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb26-124">입력</span><span class="sxs-lookup"><span data-stu-id="ecb26-124">INPUTS</span></span>

### <span data-ttu-id="ecb26-125">않아야</span><span class="sxs-lookup"><span data-stu-id="ecb26-125">None</span></span>

## <span data-ttu-id="ecb26-126">출력</span><span class="sxs-lookup"><span data-stu-id="ecb26-126">OUTPUTS</span></span>

### <span data-ttu-id="ecb26-127">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="ecb26-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ecb26-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ecb26-128">NOTES</span></span>

## <span data-ttu-id="ecb26-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecb26-129">RELATED LINKS</span></span>

[<span data-ttu-id="ecb26-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ecb26-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="ecb26-131">새로운 AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ecb26-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="ecb26-132">제거-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ecb26-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
