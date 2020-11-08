---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212720"
---
# <span data-ttu-id="bc695-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="bc695-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="bc695-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc695-102">SYNOPSIS</span></span>

<span data-ttu-id="bc695-103">복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="bc695-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc695-104">SYNTAX</span></span>

### <span data-ttu-id="bc695-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc695-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc695-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc695-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc695-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bc695-107">DESCRIPTION</span></span>

<span data-ttu-id="bc695-108">**AzRecoveryServicesVault** cmdlet은 현재 구독의 복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="bc695-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bc695-109">EXAMPLES</span></span>

### <span data-ttu-id="bc695-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bc695-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="bc695-111">선택한 구독에서 자격 증명 모음 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="bc695-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="bc695-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="bc695-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="bc695-113">선택한 구독에서 리소스 그룹의 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="bc695-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="bc695-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="bc695-115">지정 된 이름을 사용 하 여 리소스 그룹의 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="bc695-116">변수</span><span class="sxs-lookup"><span data-stu-id="bc695-116">PARAMETERS</span></span>

### <span data-ttu-id="bc695-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc695-117">-DefaultProfile</span></span>

<span data-ttu-id="bc695-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc695-119">-이름</span><span class="sxs-lookup"><span data-stu-id="bc695-119">-Name</span></span>

<span data-ttu-id="bc695-120">쿼리할 자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-120">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="bc695-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc695-121">-ResourceGroupName</span></span>

<span data-ttu-id="bc695-122">지정 된 복구 서비스 개체를 검색할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="bc695-123">태그</span><span class="sxs-lookup"><span data-stu-id="bc695-123">-Tag</span></span>

<span data-ttu-id="bc695-124">쿼리할 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-124">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="bc695-125">-태그</span><span class="sxs-lookup"><span data-stu-id="bc695-125">-TagName</span></span>

<span data-ttu-id="bc695-126">쿼리할 태그의 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-126">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="bc695-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="bc695-127">-TagValue</span></span>

<span data-ttu-id="bc695-128">쿼리할 태그의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-128">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="bc695-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc695-129">CommonParameters</span></span>
<span data-ttu-id="bc695-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc695-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc695-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc695-132">입력</span><span class="sxs-lookup"><span data-stu-id="bc695-132">INPUTS</span></span>

### <span data-ttu-id="bc695-133">않아야</span><span class="sxs-lookup"><span data-stu-id="bc695-133">None</span></span>

## <span data-ttu-id="bc695-134">출력</span><span class="sxs-lookup"><span data-stu-id="bc695-134">OUTPUTS</span></span>

### <span data-ttu-id="bc695-135">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="bc695-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="bc695-136">상속자</span><span class="sxs-lookup"><span data-stu-id="bc695-136">NOTES</span></span>
<span data-ttu-id="bc695-137">2.10.0 (<=)의 이전 버전의 Az 서비스 Get-AzRecoveryServicesVault는 잘못 된 어셈블리 참조로 인해 Az (>= 1.8.1)와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="bc695-138">최신 Az 또는 Az를 사용 하는 경우 모듈 Az 서비스를 2.11.0 또는 최신 버전으로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc695-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="bc695-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc695-139">RELATED LINKS</span></span>

[<span data-ttu-id="bc695-140">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="bc695-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="bc695-141">새로운 AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="bc695-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="bc695-142">제거-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="bc695-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
