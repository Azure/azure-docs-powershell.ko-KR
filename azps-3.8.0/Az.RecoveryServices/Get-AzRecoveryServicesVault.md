---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: b7ee6a380bf7803913f3f302bee45bad62f106b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044716"
---
# <span data-ttu-id="6074f-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6074f-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="6074f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6074f-102">SYNOPSIS</span></span>

<span data-ttu-id="6074f-103">복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="6074f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6074f-104">SYNTAX</span></span>

### <span data-ttu-id="6074f-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="6074f-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6074f-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6074f-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6074f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6074f-107">DESCRIPTION</span></span>

<span data-ttu-id="6074f-108">**AzRecoveryServicesVault** cmdlet은 현재 구독의 복구 서비스 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="6074f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6074f-109">EXAMPLES</span></span>

### <span data-ttu-id="6074f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6074f-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="6074f-111">선택한 구독에서 자격 증명 모음 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="6074f-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="6074f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="6074f-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="6074f-113">선택한 구독에서 리소스 그룹의 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="6074f-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="6074f-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="6074f-115">지정 된 이름을 사용 하 여 리소스 그룹의 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="6074f-116">변수</span><span class="sxs-lookup"><span data-stu-id="6074f-116">PARAMETERS</span></span>

### <span data-ttu-id="6074f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6074f-117">-DefaultProfile</span></span>

<span data-ttu-id="6074f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6074f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="6074f-119">-Name</span></span>

<span data-ttu-id="6074f-120">쿼리할 자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-120">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="6074f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6074f-121">-ResourceGroupName</span></span>

<span data-ttu-id="6074f-122">지정 된 복구 서비스 개체를 검색할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="6074f-123">태그</span><span class="sxs-lookup"><span data-stu-id="6074f-123">-Tag</span></span>

<span data-ttu-id="6074f-124">쿼리할 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-124">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="6074f-125">-태그</span><span class="sxs-lookup"><span data-stu-id="6074f-125">-TagName</span></span>

<span data-ttu-id="6074f-126">쿼리할 태그의 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-126">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="6074f-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="6074f-127">-TagValue</span></span>

<span data-ttu-id="6074f-128">쿼리할 태그의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-128">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="6074f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6074f-129">CommonParameters</span></span>
<span data-ttu-id="6074f-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6074f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6074f-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6074f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6074f-132">입력</span><span class="sxs-lookup"><span data-stu-id="6074f-132">INPUTS</span></span>

### <span data-ttu-id="6074f-133">않아야</span><span class="sxs-lookup"><span data-stu-id="6074f-133">None</span></span>

## <span data-ttu-id="6074f-134">출력</span><span class="sxs-lookup"><span data-stu-id="6074f-134">OUTPUTS</span></span>

### <span data-ttu-id="6074f-135">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="6074f-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="6074f-136">상속자</span><span class="sxs-lookup"><span data-stu-id="6074f-136">NOTES</span></span>

## <span data-ttu-id="6074f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6074f-137">RELATED LINKS</span></span>

[<span data-ttu-id="6074f-138">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="6074f-138">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="6074f-139">새로운 AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6074f-139">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="6074f-140">제거-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6074f-140">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
