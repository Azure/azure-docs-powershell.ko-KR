---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: f4d45cddd893ece419fab38759425bb104b64522
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994490"
---
# <span data-ttu-id="ace59-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="ace59-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="ace59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ace59-102">SYNOPSIS</span></span>
<span data-ttu-id="ace59-103">Vault 비밀 그룹에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ace59-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="ace59-104">구문</span><span class="sxs-lookup"><span data-stu-id="ace59-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="ace59-105">설명</span><span class="sxs-lookup"><span data-stu-id="ace59-105">DESCRIPTION</span></span>
<span data-ttu-id="ace59-106">비밀 그룹에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ace59-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="ace59-107">예제</span><span class="sxs-lookup"><span data-stu-id="ace59-107">EXAMPLES</span></span>

### <span data-ttu-id="ace59-108">예제 1: 자격 증명 모음 비밀 그룹 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ace59-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="ace59-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 자격 증명 모음 비밀 그룹 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ace59-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="ace59-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="ace59-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="ace59-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ace59-111">PARAMETERS</span></span>

### <span data-ttu-id="ace59-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="ace59-112">-CertificateUrl</span></span>
<span data-ttu-id="ace59-113">Key Vault에 비밀로 업로드된 인증서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="ace59-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace59-114">-Id</span><span class="sxs-lookup"><span data-stu-id="ace59-114">-Id</span></span>
<span data-ttu-id="ace59-115">Key Vault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ace59-115">Key Vault Resource Id.</span></span>

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

### <span data-ttu-id="ace59-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace59-116">CommonParameters</span></span>
<span data-ttu-id="ace59-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ace59-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace59-118">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ace59-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace59-119">입력</span><span class="sxs-lookup"><span data-stu-id="ace59-119">INPUTS</span></span>

## <span data-ttu-id="ace59-120">출력</span><span class="sxs-lookup"><span data-stu-id="ace59-120">OUTPUTS</span></span>

### <span data-ttu-id="ace59-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="ace59-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="ace59-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ace59-122">NOTES</span></span>

<span data-ttu-id="ace59-123">별칭</span><span class="sxs-lookup"><span data-stu-id="ace59-123">ALIASES</span></span>

## <span data-ttu-id="ace59-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ace59-124">RELATED LINKS</span></span>

