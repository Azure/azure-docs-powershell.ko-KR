---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491698"
---
# <span data-ttu-id="3c1b5-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3c1b5-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="3c1b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c1b5-102">SYNOPSIS</span></span>

<span data-ttu-id="3c1b5-103">Recovery Services 자격 증명 모음 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="3c1b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c1b5-104">SYNTAX</span></span>

### <span data-ttu-id="3c1b5-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c1b5-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c1b5-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c1b5-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c1b5-107">설명</span><span class="sxs-lookup"><span data-stu-id="3c1b5-107">DESCRIPTION</span></span>

<span data-ttu-id="3c1b5-108">**Get-AzRecoveryServicesVault** cmdlet은 현재 구독의 Recovery Services 자격 증명 모음 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="3c1b5-109">예제</span><span class="sxs-lookup"><span data-stu-id="3c1b5-109">EXAMPLES</span></span>

### <span data-ttu-id="3c1b5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c1b5-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="3c1b5-111">선택한 구독에서 자격 증명 모음 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="3c1b5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="3c1b5-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="3c1b5-113">선택한 구독의 리소스 그룹의 자격 증명 모음 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="3c1b5-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="3c1b5-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="3c1b5-115">첫 번째 cmdlet은 리소스 그룹의 자격 증명 모음을 지정한 이름으로 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="3c1b5-116">그런 다음 자격 증명 모음에서 MSI 정보에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="3c1b5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c1b5-117">PARAMETERS</span></span>

### <span data-ttu-id="3c1b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1b5-118">-DefaultProfile</span></span>

<span data-ttu-id="3c1b5-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c1b5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3c1b5-120">-Name</span></span>

<span data-ttu-id="3c1b5-121">쿼리할 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-121">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1b5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c1b5-122">-ResourceGroupName</span></span>

<span data-ttu-id="3c1b5-123">지정된 Recovery Services 개체를 검색할 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1b5-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c1b5-124">-Tag</span></span>

<span data-ttu-id="3c1b5-125">쿼리할 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-125">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1b5-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="3c1b5-126">-TagName</span></span>

<span data-ttu-id="3c1b5-127">쿼리할 태그의 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-127">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1b5-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="3c1b5-128">-TagValue</span></span>

<span data-ttu-id="3c1b5-129">쿼리할 태그의 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-129">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1b5-130">CommonParameters</span></span>
<span data-ttu-id="3c1b5-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1b5-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1b5-133">입력</span><span class="sxs-lookup"><span data-stu-id="3c1b5-133">INPUTS</span></span>

### <span data-ttu-id="3c1b5-134">없음</span><span class="sxs-lookup"><span data-stu-id="3c1b5-134">None</span></span>

## <span data-ttu-id="3c1b5-135">출력</span><span class="sxs-lookup"><span data-stu-id="3c1b5-135">OUTPUTS</span></span>

### <span data-ttu-id="3c1b5-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="3c1b5-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="3c1b5-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c1b5-137">NOTES</span></span>
<span data-ttu-id="3c1b5-138">Get-AzRecoveryServicesVault Az.RecoveryServices(<=2.10.0)의 경우 잘못된 어셈블리 참조로 Az.Accounts(>=1.8.1)를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="3c1b5-139">최신 Az 또는 Az.Accounts를 사용하는 경우 모듈 Az.RecoveryServices를 2.11.0 이상으로 업그레이드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="3c1b5-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c1b5-140">RELATED LINKS</span></span>

[<span data-ttu-id="3c1b5-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3c1b5-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="3c1b5-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3c1b5-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="3c1b5-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3c1b5-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
