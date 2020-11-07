---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: d541c943c8dc9779cdf340440078ca2fd2fb36e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875290"
---
# <span data-ttu-id="dce37-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="dce37-101">Get-AzProfile</span></span>

## <span data-ttu-id="dce37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dce37-102">SYNOPSIS</span></span>
<span data-ttu-id="dce37-103">설치 된 모듈에서 지원 되는 서비스 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dce37-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="dce37-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dce37-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="dce37-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dce37-105">DESCRIPTION</span></span>
<span data-ttu-id="dce37-106">설치 된 모듈에서 지원 되는 서비스 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dce37-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="dce37-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dce37-107">EXAMPLES</span></span>

### <span data-ttu-id="dce37-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dce37-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="dce37-109">KeyVault 모듈에서 지원 되는 서비스 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="dce37-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="dce37-110">변수</span><span class="sxs-lookup"><span data-stu-id="dce37-110">PARAMETERS</span></span>

### <span data-ttu-id="dce37-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="dce37-111">-ListAvailable</span></span>
<span data-ttu-id="dce37-112">설치 된 모듈에서 지원 되는 모든 서비스 프로필 나열</span><span class="sxs-lookup"><span data-stu-id="dce37-112">List all service profiles supported by installed modules</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce37-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="dce37-113">-ModuleName</span></span>
<span data-ttu-id="dce37-114">확인할 모듈의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dce37-114">The name of the module to check</span></span>

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

### <span data-ttu-id="dce37-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce37-115">CommonParameters</span></span>
<span data-ttu-id="dce37-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce37-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce37-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dce37-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce37-118">입력</span><span class="sxs-lookup"><span data-stu-id="dce37-118">INPUTS</span></span>

### <span data-ttu-id="dce37-119">않아야</span><span class="sxs-lookup"><span data-stu-id="dce37-119">None</span></span>

## <span data-ttu-id="dce37-120">출력</span><span class="sxs-lookup"><span data-stu-id="dce37-120">OUTPUTS</span></span>

### <span data-ttu-id="dce37-121">CommonModule. m m/. w i m/. m m m 프로필</span><span class="sxs-lookup"><span data-stu-id="dce37-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="dce37-122">상속자</span><span class="sxs-lookup"><span data-stu-id="dce37-122">NOTES</span></span>

## <span data-ttu-id="dce37-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dce37-123">RELATED LINKS</span></span>
